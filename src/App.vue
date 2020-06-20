<template>
  <div id="app">
    <LandingPage/>
    <animatedBackground/>
  </div>
</template>

<script>
import LandingPage from './components/LandingPage.vue'
import animatedBackground from './components/animatedBackground.vue'
export default {
  name: 'App',
  components: {
    LandingPage,
    animatedBackground,
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
</style>
