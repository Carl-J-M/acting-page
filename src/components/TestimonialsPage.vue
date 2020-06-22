<template>
    <div class="pageContainer" id="testimonals">
        <h1></h1>
    </div>
</template>
<script>
export default {
    data(){

    } 
}
</script>
<style scoped>
    .pageContainer {
        position: relative;
        left: 0px;
        width: 100vw;
        height:200vh;
        animation: fadebg infinite 20s, ease-in-out 0s;
            -webkit-mask-image: -webkit-gradient(linear, left top, left bottom, 
    from(rgba(0,0,0,1)), to(rgba(0,0,0,0)));
        z-index: 1;
        font-family: 'Montserrat', sans-serif;
        color: white;
    }
    
@keyframes  fadebg {
      0% { 
          background-color:rgb(7, 108, 224);
          
      }
      35% {
          background-color:rgb(255, 127, 68);
      }
      55% {
          background-color: rgb(9, 1, 43);
      }
      85% {
          background-color: rgb(9, 1, 43);
      }
      100% {
          background-color:rgb(7, 108, 224);
      }
  }

</style>