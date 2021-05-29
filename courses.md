---
layout: courses
title: Courses
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
   max-width: 1000px;
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
   width: 50%;
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
   }
   .chip img {
   float: left;
   margin: 0 10px 0 -25px;
   height: 50px;
   width: 50px;
   border-radius: 50%;
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
   color: white;
   background-color: #000;
   text-align: center;
   cursor: pointer;
   width: 100%;
   font-size: 18px;
   }
   .card button:hover {
   opacity: 0.7;
   }
   body {font-family: Arial, Helvetica, sans-serif;}
   .image-container-1 {
   background-image: url("/assets/img/course-k8s.png");
   background-size: cover;
   position: relative;
   height: 300px;
   }
   .text {
   background-color: white;
   color: black;
   font-size: 4vw; 
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
</style>
<!-- MAIN (Center website) -->
<div class="main">
   <hr>
   <!-- Portfolio Gallery Grid -->
   <div class="row">
      <div class="column">
            <div class="content">
                <div class="image-container-1">
                    <div class="text">OPENSHIFT</div>
                </div>
                <h3>Arquitetura cloud e CI/CD</h3>
                <p>Lorem ipsum dolor sit amet, tempor prodesset eos no. Temporibus necessitatibus sea ei, at tantas oporteat nam. Lorem ipsum dolor sit amet, tempor prodesset eos no.</p>
                <div class="chip">
                    <img src="https://www.w3schools.com/howto/img_avatar.png" alt="Person" width="96" height="96">
                    Réberth Rodrigues
                </div>
                <p><button>Comprar agora</button></p>
            </div>
      </div>
      <div class="column">
            <div class="content">
                <div class="image-container-1">
                    <div class="text">OPENSHIFT</div>
                </div>
                <h3>Arquitetura cloud e CI/CD</h3>
                <p>Lorem ipsum dolor sit amet, tempor prodesset eos no. Temporibus necessitatibus sea ei, at tantas oporteat nam. Lorem ipsum dolor sit amet, tempor prodesset eos no.</p>
                <div class="chip">
                    <img src="https://www.w3schools.com/howto/img_avatar.png" alt="Person" width="96" height="96">
                    Réberth Rodrigues
                </div>
                <p><button>Comprar agora</button></p>
            </div>
      </div>
            <div class="column">
            <div class="content">
                <div class="image-container-1">
                    <div class="text">OPENSHIFT</div>
                </div>
                <h3>Arquitetura cloud e CI/CD</h3>
                <p>Lorem ipsum dolor sit amet, tempor prodesset eos no. Temporibus necessitatibus sea ei, at tantas oporteat nam. Lorem ipsum dolor sit amet, tempor prodesset eos no.</p>
                <div class="chip">
                    <img src="https://www.w3schools.com/howto/img_avatar.png" alt="Person" width="96" height="96">
                    Réberth Rodrigues
                </div>
                <p><button>Comprar agora</button></p>
            </div>
      </div>
      <div class="column">
            <div class="content">
                <div class="image-container-1">
                    <div class="text">OPENSHIFT</div>
                </div>
                <h3>Arquitetura cloud e CI/CD</h3>
                <p>Lorem ipsum dolor sit amet, tempor prodesset eos no. Temporibus necessitatibus sea ei, at tantas oporteat nam. Lorem ipsum dolor sit amet, tempor prodesset eos no.</p>
                <div class="chip">
                    <img src="https://www.w3schools.com/howto/img_avatar.png" alt="Person" width="96" height="96">
                    Réberth Rodrigues
                </div>
                <p><button>Comprar agora</button></p>
            </div>
      </div>


      
   </div>
   <!-- END GRID -->
</div>

