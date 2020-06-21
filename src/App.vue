<template>
  <div id="app">
        <Reveal id="slide">
      <a id="home" href="#">
        <span>Home</span>
      </a>
      <a id="testimonials" href="#">
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
    <LandingPage/>
    <animatedBackground/>
      </main>

  </div>
</template>

<script>
import LandingPage from './components/LandingPage.vue'
import animatedBackground from './components/animatedBackground.vue'
import { Reveal } from 'vue-burger-menu'
export default {
  name: 'App',
  components: {
    LandingPage,
    animatedBackground,
    Reveal
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

    overflow: hidden;
    box-sizing: border-box;

}
#slide {
  position: sticky;
  z-index: 10;
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
      background-color: rgb(0, 0, 0); /* Black*/
      
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
</style>
