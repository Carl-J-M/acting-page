<template>
  <div id="app">
    <Reveal id="slide" :closeOnNavigation="true">
      <a id="home" href="#homepage">
        <span>Home</span>
      </a>
      <a id="test" href="#testimonials">
        <span>Testimonials</span>
      </a>
      <a id="about" href="#">
        <span>About</span>
      </a>
      <a id="contact" href="#">
        <span>Contact</span>
      </a>
    </Reveal>

    <main id="page-wrap">
      <LandingPage id="homepage"/>
      <animatedBackground/>
      <TestimonialsPage id="testimonials"/>
    </main>
  </div>
</template>

<script>
import LandingPage from './components/LandingPage.vue'
import animatedBackground from './components/animatedBackground.vue'
import TestimonialsPage from './components/TestimonialsPage.vue'

import { Reveal } from 'vue-burger-menu'
export default {
  name: 'App',
  components: {
    LandingPage,
    animatedBackground,
    Reveal,
    TestimonialsPage

  }
}
</script>

<style>
* {
  margin: 0px;
  padding: 0px;
}
#app {
    position: absolute;

    top: 0px;
    left: 0px;

    box-sizing: border-box;

}
#slide {
  position: fixed;
  z-index: 100;
  /* overflow-y: hidden; */
}

    .bm-burger-bars {
      background-color: #ffffff;
    }

        .bm-menu {
      height: 100vh; /* 100% Full-height */
      width: 0; /* 0 width - change this with JavaScript */
      position: fixed; /* Stay in place */
      z-index: 1000; /* Stay on top */
      font-family: 'Montserrat', sans-serif;
      top: 0;
      left: 0;
      background-color: rgb(0, 0, 0); 
      /* animation: fadebgfill infinite 20s, ease-in-out 0s; */
      overflow-x: hidden; /* Disable horizontal scroll */
      padding-top: 60px; /* Place content 60px from the top */
      transition: 0.5s; /*0.5 second transition effect to slide in the sidenav*/
    }
        .bm-cross {
      background: #000000;
    }
    .bm-item-list {
      color: #000000;
      margin-left: 10%;
      font-size: 20px;
    }

    #home {

    }

@keyframes  fadebg {
      0% {
          
          background-color:rgb(65, 135, 192);
          /* background-color: rgba(153, 0, 255, 0.822); */
          
      }
      25% {
          
          background-color:rgb(204, 140, 2);
          /* background-color: rgba(153, 0, 255, 0.822); */
      }
      /* 30% {
          background-color:rgb(21, 44, 16);
      }
      35% {
          background-color:rgb(21, 44, 16);
      } */
      40% {
          background-color: rgb(9, 1, 43);
      }
      85% {
          background-color: rgb(9, 1, 43);
      }
      100% {
          /* background-color: rgba(209, 78, 2, 0.295); */
          background-color:rgb(65, 135, 192);
      }
  }

    
</style>
