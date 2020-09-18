---
layout: post
title: Microsserviços com poder de negócio
subtitle: Apache Camel + Drools + Openshift + Spring-Boot
cover-img: /assets/img/micro.jpg
thumbnail-img: /assets/img/micro-thumb.jpg
share-img: /assets/img/micro.jpg
tags: [redhat ,openshift ,camel ,drools ,springboot ,containers ,microservices ,kieserver ,jboss  ]
---

Uma das poderosas ferramentas de automação de tomada de decisão:  RedHat Decision Manager ou simplesmente Drools (em sua versão de  comunidade). Cabe muito bem e  obrigado na arquitetura de container.  Utilizando o Red Hat Openshift e Spring-boot.

Cada vez mais  simples desenvolver uma API REST com rotas Camel. Regras de negócio  podem ser incorporadas ao Spring-Boot de duas formas. A primeira opção:  Kie server, o serviço de execução de drools. Utilizada em conjunto com  uma aplicação em microsserviço Camel e Spring-boot. Temos um cenário de  aplicações escaláveis e distribuídas.

![](/assets/img/micro1.png)

A segunda opção: utilizando drools com integração contínua. As regras são compiladas em tempo de execução. Não sendo necessário novo deploy  ou reboot de aplicações. Mantendo uma arquitetura distribuída e de  microsserviços. 

Com equipes de negócio interagindo com equipe de  desenvolvimento. Diminuindo cada vez mais a complexidade de negócio de  sua aplicação backend. Podendo utilizar features do drools, como  planilha de excel de regras de negócio incorporada diretamente ao código da aplicação.

![](/assets/img/micro2.png)

**Referências**

- https://www.openshift.com/
- https://camel.apache.org/
- https://www.redhat.com/pt-br/technologies/jboss-middleware/decision-manager