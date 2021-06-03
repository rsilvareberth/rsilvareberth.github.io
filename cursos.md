---
layout: courses
title: Cursos
subtitle: Grade de cursos disponíveis
---
<style>
   * {
   box-sizing: border-box;
   }
   body {
   background-color: #f1f1f1;
   padding: 20px;
   font-family: Arial;
   }
   /* Center website */
   .main {
   max-width: 1200px;
   margin: auto;
   }
   h1 {
   font-size: 50px;
   word-break: break-all;
   }
   .row {
   margin: 8px -16px;
   }
   /* Add padding BETWEEN each column */
   .row,
   .row > .column {
   padding: 8px;
   }
   /* Create four equal columns that floats next to each other */
   .column {
   float: left;
   width: 33%;
   }
   /* Clear floats after rows */ 
   .row:after {
   content: "";
   display: table;
   clear: both;
   }
   /* Content */
   .content {
   background-color: white;
   padding: 10px;
   }
   /* Responsive layout - makes a two column-layout instead of four columns */
   @media screen and (max-width: 900px) {
   .column {
   width: 50%;
   }
   }
   /* Responsive layout - makes the two columns stack on top of each other instead of next to each other */
   @media screen and (max-width: 600px) {
   .column {
   width: 100%;
   }
   }
   .chip {
   display: inline-block;
   padding: 0 25px;
   height: 50px;
   font-size: 16px;
   line-height: 50px;
   border-radius: 25px;
   background-color: #f1f1f1;
   margin-top: 10px;
   margin-bottom: 10px;
   }
   .chip img {
   float: left;
   margin: 0 10px 0 -25px;
   height: 50px;
   width: 50px;
   border-radius: 50%;
   }
   .chip-footer{ 
    margin-left: 10px;
   }
   .card {
   box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
   max-width: 300px;
   margin: auto;
   text-align: center;
   font-family: arial;
   }
   .price {
   color: grey;
   font-size: 22px;
   }
   .column button {
   border: none;
   outline: 0;
   padding: 12px;
   color: black;
   background-color: #33ccff;
   text-align: center;
   cursor: pointer;
   width: 100%;
   font-size: 18px;
   margin-top: 12px;
   }
   .card button:hover {
   opacity: 0.7;
   }
   body {font-family: Arial, Helvetica, sans-serif;}
   .image-container-1 {
   background-image: url("/assets/img/curso-img.png");
   background-size: cover;
   position: relative;
   height: 250px;
   }
   .text {
   background-color: white;
   color: black;
   font-size: 3vw; 
   font-weight: bold;
   margin: 0 auto;
   padding: 10px;
   width: 80%;
   text-align: center;
   position: absolute;
   top: 50%;
   left: 50%;
   transform: translate(-50%, -50%);
   mix-blend-mode: screen;
   }

   .label-img {
   background-color: red;
   color: black;
   font-size: 1vw; 
   font-weight: bold;
   margin: 0 auto;
   padding: 10px;
   width: 35%;
   text-align: center;
   position: absolute;
   top: 10%;
   left: 20%;
   transform: translate(-60%, -50%);
   mix-blend-mode: screen;
   }

   .label {
    color: white;
    font-size: 1.2vw; 
    padding: 8px;
   }

.success {background-color: #04AA6D;} /* Green */
.info {background-color: #2196F3; font-weight: bold;} /* Blue */
.warning {background-color: #ff9800;} /* Orange */
.danger {background-color: #f44336;} /* Red */
.other {background-color: #e7e7e7; color: black;} /* Gray */
.go {background-color: #2196F3; margin-left: 10px; font-weight: bold;} /* Blue */

.small-test-course{
    height: 110px;
}
</style>
<!-- MAIN (Center website) -->


<div class="main">
<hr>
<!-- Portfolio Gallery Grid -->
    <div class="row">
        <div class="column">
            <div class="content">
                <a style="display:block" href="">
                    <div class="image-container-1">
                        <div class="text">Design API</div>
                        <div class="label-img">Esgotado</div>
                    </div>
                </a>
                <h4>Contract first</h4>
                <div class="small-test-course">
                    <span>Abordagem contract first e cloud first no desenvolvimento de uma API. Desenvolvimento com base no valor agregado e performance de times.</span>
                </div>
                <div class="chip">
                    <img src="/assets/img/profile_cropped.jpg" alt="Person" width="1728" height="2304">
                    Réberth Rodrigues
                </div>
                    <div class="row">
                        <div class="chip-footer">
                        <span class="label success">Iniciante</span>
                        </div>
                        <div class="cont">
                        <span class="label other">Gratuito</span>
                        </div>
                        <div class="cont">
                        <a style="display:block" href="">                        
                            <span class="label go">Iniciar</span>
                        </a>
                        </div>
                    </div>
            </div>          
        </div>
        <div class="column">
            <div class="content">
                <a style="display:block" href="">
                    <div class="image-container-1">
                        <div class="text">Quarkus</div>
                        <div class="label-img">Esgotado</div>
                    </div>
                </a>
                <h4>Quarkus</h4>
                <div class="small-test-course">
                    <span>Quarkus é uma Stack Java, nativa para Kubernetes, feita sob medida para OpenJDK e GraalVM, criada com as melhores bibliotecas Java.</span>
                </div>
                <div class="chip">
                    <img src="/assets/img/profile_cropped.jpg" alt="Person" width="1728" height="2304">
                    Réberth Rodrigues
                </div>
                    <div class="row">
                        <div class="chip-footer">
                        <span class="label success">Intermediário</span>
                        </div>
                        <div class="cont">
                        <span class="label other">Valor</span>
                        </div>
                        <div class="cont">
                        <a style="display:block" href="">
                            <span class="label go">Iniciar</span>
                        </a>
                        </div>
                    </div>
            </div>          
        </div>
        <div class="column">
            <div class="content">
                <a style="display:block" href="">
                    <div class="image-container-1">
                        <div class="text">Openshift</div>
                        <div class="label-img">Esgotado</div>
                    </div>
                </a>
                <h4>Openshift 4</h4>
                <div class="small-test-course">
                    <span>Fundamentos e conceitos básicos que você precisará para construir um cluster simples e começar a implantar e gerenciar aplicações cloud native</span>
                </div>
                <div class="chip">
                    <img src="/assets/img/profile_cropped.jpg" alt="Person" width="1728" height="2304">
                    Réberth Rodrigues
                </div>
                    <div class="row">
                        <div class="chip-footer">
                        <span class="label success">Intermediário</span>
                        </div>
                        <div class="cont">
                        <span class="label other">Valor</span>
                        </div>
                        <div class="cont">
                        <a style="display:block" href="">
                            <span class="label go">Iniciar</span>
                        </a>
                        </div>
                    </div>
            </div>          
        </div>        
   </div>
   <!-- END GRID -->
</div>

