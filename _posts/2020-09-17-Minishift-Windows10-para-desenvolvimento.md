---
layout: post
title: Passo a passo Minishift/Windows10
subtitle: preparação de ambiente de orquestração de container Openshift
cover-img: /assets/img/ocp.png
thumbnail-img: /assets/img/ocp-thumb.png
share-img: /assets/img/ocp.png
tags: [redhat ,openshift , containers ,microservices , okd, minishift openshift origin  ]
---



Criar um ambiente de desenvolvimento para o Openshift pode ser um pouco complexo no início. Por isso vou mostrar um passo a passo sem surpresas neste post.

Neste contexto, irei mostrar apenas a instalação da plataforma Openshift em sua versão open source Minishift.

Antes de tudo. Vamos aos requisitos:

`Windows 10 PRO build >= 2004. Caso tenha a versão Home, aconselho fortemente realizar esta atualização. Pois a versão Home não está preparada para trabalhar com virtualização da maneira adequada.` 

`Memória RAM? Vamos sim precisar! Separe 12gb de RAM para subir a plataforma. Claro que esta memória também vai servir para os containers que você vai criar. Ou seja, você tem que ter 16gb de RAM na sua máquina. 4gb reservados para o Windows. Vale o investimento em memória RAM e também SSD caso possível. É muito? vale fazer um upgrade. Pois os serviços de Openshift Online vão te custar pelo menos 50 dólares mensais com uma versão mais básica. Deploy do Openshift em alguma cloud? Vamos deixar esta opção para outro post. Como estamos falando em ambiente de desenvolvimento, com apenas um node, sem clusters. Vale termos um ambiente de estudo. `

Neste momento aconselho utilizar Hyper-V ao inves de virtualbox. Primeiro, você terá o recurso nativo compatível com o Windows. Segundo, se você também quer manter um ambiente com o Docker instalado. Não haverá problemas. Uma vez que existem inconsistencias com Hyper-V e VirtualBox rodando no Windows. Caso o VirtualBox esteja instalado, recomendo desinstalá-lo. 

**Disclaimer:**

*A escolha do Hyper-V é pelo simples fato de que você enfrentará muitos problemas com Virtualbox. A escolha não está relacionada a nenhum favoritismo com a Microsoft.*

Dito isto. Podemos continuar. Neste caso, o próximo passo é habilitar o Hyper-V e configurá-lo.

Abra o powershell como administrador:

Execute o comando para habilitar o Hyper-V

`Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V -All`

Realize reboot da máquina.

Abra o powershell como administrador.

Verifique a política de execução  de comandos .

`Get-ExecutionPolicy` 

Caso esteja diferente de AllSigned. Rode esta linha de comando para desabilitar política de segurança:

`Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))`

Verifique novamente:

`Get-ExecutionPolicy` 

Feito isto, vamos iniciar a instalação do minishift:

`choco install -y minishift`

`minishift version`(cheque a versão instalada).

`choco install -y kubernetes-cli`

`choco install -y openshift-cli`

Crie uma adaptador de rede virtual no Hyper-V (continue no powershell como administrador) . 

Verifique os adaptadores existentes:

`Get-NetAdapter`

No meu caso, o nome do meu adaptador real de rede é: "Ethernet" e virtual "ExternalSwitch".

`New-VMSwitch -name <nomeNovoAdaptadorVirtual> -NetAdapterName <nomeAdaptadorReal> -AllowManagementOS $true`

Rode novamente o comando para confirmar a criação do adaptador

`Get-NetAdapter`

![Adaptador externo Hyper-V](/assets/img/ocp1.png)

Configure o minishift para sempre utilizar o switch externo criado, 12GB de memória RAM  e o driver de virtualização Hyper-V:

`minishift config set hyperv-virtual-switch "<nomeNovoAdaptadorVirtual>"`

`minishift config set vm-driver hyperv`

`minishift config set memory 12GB`

Crie um usuário do Windows **não administrador**. E tenha certeza de atribuí-lo ao grupo "Hyper-V Administrators" ou correspondente na linguagem instalada. Realize a operação abrindo o assistente "lusrmgr.msc." via executar. Pois devido à linguagem, os nomes podem variar.

Após isto, basta iniciar o powershell com o usuário criado. 

Verifique se o usuário escolhido possui o grupo administrador Hyper-V

 `Get-LocalGroupMember -Group "Hyper-V Administrators"`

Inicie o minishift:

 `minishift start` 

Para acompanhar logs de inicialização, rode com o parâmetro adicional:

 `minishift start --show-libmachine-logs -v5`

Você deve ver um log inicial semelhante a este:

![Log inicial](/assets/img/ocp-log1.png)

E final semelhante a este:

![Log final](/assets/img/ocp-log2.png)

Resultado final no navegador:

Voila!!!!

![Log final](/assets/img/ocp-main-page.png)

**Troubleshooting**

Em caso de problemas ao obter endereço de IP do minishift ao iniciar o node. Certifique-se de ter apenas um cliente SSH instalado no Windows. Se você possui o cliente do git. Desinstale o OpenSSH nativo do Windows 10 com o comando:

`choco uninstall OpenSSH`

Bem como também do adaptador virtual do Hyper-V tipo externo.

**Referências**

- https://www.openshift.com/
- https://www.okd.io/minishift/
- https://docs.microsoft.com/pt-br/virtualization/hyper-v-on-windows/quick-start/enable-hyper-v