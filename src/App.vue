<template>
  <Navbar />
  <Home />


  <section class="about-us" id="about-us">
    <article class="about-clogo">

      <div class="about-logo">
        <img src="@/assets/logo_340.webp" alt="">
      </div>

    </article>

    <article class="about-content">
      <div class="about-item">
        <h1>¿QUIENES SOMOS?</h1>
        <p>
          Somos una empresa dedicada a brindar servicios marítimos portuarios como procesamiento de recursos
          hidrobiológicos, offshore, pesca, trasporte marítimo y abastecimiento, así como a actividades de prestación que
          sean necesarias para la explotación de los puertos, asociadas a actividades comerciales asociadas al tráfico
          marítimo.
        </p>
      </div>
      <div class="about-item">
        <h1>MISIóN
        </h1>
        <p>
          Brindar servicios de alta calidad y eficiencia en el rubro marítimo, que den soluciones y satisfagan las
          necesidades de nuestros clientes, manteniendo un alto estándar de gestión de los recursos.
          <br><br>
          Nuestra prioridad es la seguridad, eficiencia, regularidad, continuidad y no discriminación en el ámbito
          acuático.
        </p>
      </div>
      <div class="about-item">
        <h1>Visión</h1>
        <p>
          Ser una empresa líder en el sector marítimo y reconocida en América Latina, basada en altos estándares de
          calidad, seguridad, cuidado del medio ambiente y cumplimiento de objetivos.
        </p>
      </div>
    </article>

  </section>



  <section class="products bg-line">
    <h1>
      Nuestros Productos
    </h1>
  </section>

    <Products/>

  <section class="services bg-line">
    <h1>
      Servicios
    </h1>
  </section>


</template>

<script>

import Navbar from '@/components/Navbar.vue';
import Home from '@/components/Home.vue';
import Products from '@/components/Products.vue';
export default {
  name: 'App',
  components: {
    Navbar,
    Home,
    Products
  }
}


</script>

<style>
/* Root */
:root {}

@font-face {
  font-family: 'Poppins';
  src: url('@/assets/font/Poppins/Poppins-Medium.ttf');
  font-display: swap;
}

/* General */
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

ul {
  list-style-type: none;
}

a {
  text-decoration: none;
}

img {
  width: 100%;
  height: 100%;
}

html {
  scroll-behavior: smooth;
  -webkit-tap-highlight-color: transparent;
}

body {
  font-family: 'Poppins', sans-serif;
}


/* About */


.services,
.products,
.about-clogo {
  width: 100%;
  height: 150px;
  background: #1ea0c3;
  display: flex;
  justify-content: center;
  align-items: center;
}


.about-logo {
  width: 300px;
}

.about-content{
  display: flex;
  align-items: flex-start;
  justify-content: center;
  flex-wrap: wrap;
  padding: 5rem 0;
  gap: 50px;
} 
.about-item{
  width: 400px;
  display: flex;
  flex-direction: column;
  gap: 10px;
}
.about-item h1{
  text-align: center;
  text-transform: uppercase;
}
.about-item p{
  font-size: 13.5px;
  color: rgb(0, 0, 0, .5);
}

@media screen and (max-width: 865px) {
  .about-item{
    width: 90%; 
    text-align: center; 
  }
}

/* Productos */
.bg-line h1{
  font-size: 35px;
  text-transform: uppercase;
}

@media screen and (max-width: 450px) {
  .bg-line h1{
    font-size: 20px;
  }
}
</style>
