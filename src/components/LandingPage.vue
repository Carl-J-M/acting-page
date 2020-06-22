<template>
  <div class="pageContainer">
    
      <div>
          <div id="demo">
            <!-- <button v-on:click="show = !show" class="demo">
              <div v-if="show" class="findoutmore">TESTIMONIALS</div>
              <div v-else class="sticky home">HOME</div>
            </button> -->
            <transition name="fade">
              <div key=1 v-if="show" class="headingContainer">
                            <h1 class="name">{{details.name}}</h1>
                            <!-- <img class="headshot" src="../assets/headshot.jpg" width="190" height="auto"/> -->
                            <div class="infoContainer">
                            <!-- <h2 class="title">{{details.title}}</h2> -->
                            <div class="phrase">{{details.phrase}}</div>
                            </div>
              </div>
            </transition>

          </div>
      </div>
  </div>
</template>

<script>
export default {
  name: 'LandingPage',
    data(){
    return {
      details: {
        name: "SOPHIE MENSAH",
        title: "Actor & Acting Teacher, London",
        phrase: "You don’t need to go to drama school to be a professional actor but you do need to work hard on your craft."
      },
      bio: "Sophie Mensah is a London based British actress and acting coach with a BA HONS in Acting from the East15 Acting School and and MA in 'Actor Training and Coaching' with a distinction from The Royal Central School of Speech and Drama. As well as private coaching with established and up and coming actors, Sophie has worked as an visiting acting teacher at The Royal Central School of Speech and Drama, St Mary's University, East15 Acting School and many more.",
      show: true,
      testimonal: [
       {message: "I owe so much to this amazing lady right here, one of the best lecturers I’ve ever had. Helped me become so confident with text analysis (considering it’s not my strong point at all), broke it down & analysed everything step by step. Prepared me so well for the practical side!” - Vaneeka (Student Actor)"} ,
       {message: "Arguably the best teacher I've had, has taught me very useful techniques I now use as main stay work! Get in contact!” - Aiden (Student Actor)"},
       {message: "Spent an amazing day working with Sophie. One of the most qualified trainers I know with such a refreshing approach to performance! - Lucy Aarden(Actress)"} ,
       {message: "To all my actor/actress friends :) couldn’t recommend her more - Juliana (Actress)"} ,
       {message: "Log book work was useful, Sophie was incredible - (Student Actor)"},
       {message:  "Sophie is a talent and a joy to work with. Actors, if you're looking for an acting coach... - Darren A. Furniss (Director and Filmmaker)"},
       {message: "Terrific actress. Focus, attention to detail and work ethic are what you want and a lovely person. - Adam Christopher (Director)"} 

      ]
      
    }
  }

}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .pageContainer {
    position: relative;
    width: 100vw;
    height: 100vh;
    /* background-image: url("../assets/studio.jpg"); */
    background-size: 100% 100%;
    font-family: 'Roboto', sans-serif;
    z-index: 2;
  }
  .headingContainer {
    position: absolute;
    display: flex;
    flex-direction: column;
    justify-content: center;
    min-height: 100vh;
    width: 100vw;
    color: white;
    background: rgba(241, 211, 39, 0.459); 
    animation: fadebg infinite 20s, ease-in-out 0s;
    font-family: 'Montserrat', sans-serif;
    margin-left: 0em;
    z-index: 1;
                  -webkit-mask-image: -webkit-gradient(linear, left bottom, left top, 
    from(rgba(0,0,0,1)), to(rgba(0,0,0,0)));

  }
  .testimonialContainer {
    position: absolute;
    display: flex;
    flex-wrap: wrap;
    height: 100vh;
    width: 100vw;
    left: 0; 
    right: 0; 
    margin-left: auto; 
    margin-right: auto; 
    /* background-color: rgb(55, 248, 184); */
  }
  .testimonial {
    width: 100%;
    padding: 2em 2em;
    height: auto;
    text-align: center;
    font-size: 1em;
    font-style: italic;
    vertical-align: middle;
    color: black;
    background-color: white;
    z-index: 1;
        border-bottom: dashed black 0.21em;

        

    /* clip-path: polygon(50% 0%, 61% 35%, 98% 35%, 68% 57%, 79% 91%, 50% 70%, 21% 91%, 32% 57%, 2% 35%, 39% 35%); */
  }
  .name {
    position: absolute;
    font-size: 7em;
    left: 0px;;
    top: 5vh;
    width: 100%;
    padding-bottom: 1em;
    letter-spacing: 0.4em;
    font-weight: 800;
    z-index: 30;
    text-align: right;
  }
  .title {
    position: absolute;
    bottom: 0px;
    font-size: 0.8em; 
     margin: 0 auto;   
     padding-bottom: 0.1em;
     text-align: left;
     font-weight: 100;

  }
  .headshot {
    /* -webkit-box-shadow: 4px 10px 14px 0px rgba(0,0,0,0.75);
    -moz-box-shadow: 4px 10px 14px 0px rgba(0,0,0,0.75);
    box-shadow: 4px 10px 14px 0px rgba(0,0,0,0.75); */
     margin: 0 auto;
     
     filter: grayscale(); 
     border-radius: 3%;
     /* filter: grayscale(); */
  }
  .phrase {
    position: absolute;
    font-size: 1.5em;
    line-height: 1em;
    text-align: right;
    font-style: italic;
    /* margin: 0 auto; */
    width: 30vw;
    bottom: 5vh;
    right: 5vw;
    /* background-color: rgba(255, 255, 255, 0.521); */
    padding: 0.4em;
    /* clip-path: polygon(50% 0%, 61% 35%, 98% 35%, 68% 57%, 79% 91%, 50% 70%, 21% 91%, 32% 57%, 2% 35%, 39% 35%); */
    border-radius: 1em;
    font-family: 'Roboto', sans-serif;
    color: white;
    font-weight: 100;
    z-index: 30;
  }
  .demo {

  position: absolute; 
  left: 0; 
  right: 0; 
  bottom: 0;
  margin-left: auto; 
  margin-right: auto; 
  width: 10em;

    border: none;
    /* padding: 1rem 1rem; */
    text-decoration: none;
    /* color: black; */
    font-family: sans-serif;
    font-size: 1em;
    line-height: 1;
    cursor: pointer;
    outline-color: none;
  background-color: rgba(255, 255, 255, 0);
    -webkit-user-select: none; /* Chrome/Safari */        
    -moz-user-select: none; /* Firefox */
    -ms-user-select: none; /* IE10+ */

    margin-bottom: 1em;
    z-index: 2;
    
  }
.fade-enter-active,
.fade-leave-active {
    transition: all 1.5s
}

.fade-enter,
.fade-leave-to {
    opacity: 0;
    /* transform: translateY(100vh); */
}
.bio {
  position: absolute; 
  left: 0; 
  right: 0; 
  bottom: 20vh;
  margin-left: auto; 
  margin-right: auto; 
  width: 80vw;
  color: black;
  text-align: center;
  font-family: 'Roboto', sans-serif;
  font-size: 1em;
  background-color: black;
  padding: 2em;
}
li { 
  list-style-type: none;
}
button:focus {outline:0;}

.sticky {
  position: fixed;
}

.home {
  /* background-color: transparent; */
  color: black;
  padding: 1em;
  min-width: 10vw;
  left: 0px;
  bottom: 0px;
      -webkit-box-shadow: 4px 10px 14px 0px rgba(0,0,0,0.75);
    -moz-box-shadow: 4px 10px 14px 0px rgba(0,0,0,0.75);
    box-shadow: 4px 10px 14px 0px rgba(0,0,0,0.75);

}
.home:hover {
  color: black;
  /* background-color: white; */
}
.findoutmore {
  border-radius: 1em;
  height: 1em;
  padding: 1em;
  /* background-color: rgba(255, 255, 255, 0.521); */
}
.findoutmore:hover {
  background-color: transparent;
  /* color: black; */
}
.testimonialHeader {
  position: absolute;
  z-index: 2;  
  top: 2em;
  left: 0; 
  right: 0; 
  width: 10em;
  margin-left: auto; 
  margin-right: auto; 
}
.infoContainer {
  /* background-color: rgba(255, 255, 255, 0.349); */
  display: flex;
  flex-direction: column;
  padding: 1.1em;
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
