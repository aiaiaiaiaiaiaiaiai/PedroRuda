<template>
   <Carousel :items-to-show="1" :wrap-around="true">
    <Slide v-for="component in componentNames" v-bind:is="component" :key="component">
      <div class="carousel__item">
        <component v-bind:is="component"></component>
      </div>
    </Slide>

    <template #addons>
      <Navigation />
    </template>
  </Carousel>
  
</template>

<script>

import { Carousel, Navigation, Slide } from 'vue3-carousel';
import Page1 from './components/Page1.vue'
import Page2 from './components/Page2.vue'
import Page3 from './components/Page3.vue'
import Page4 from './components/Page4.vue'
import Page5 from './components/Page5.vue'
import Page6 from './components/Page6.vue'


import 'vue3-carousel/dist/carousel.css';

var sound = new Audio('/sound.mp3');

export default {
  name: 'App',
  components: {
    Carousel,
    Slide,
    Navigation,
    Page1,
    Page2,
    Page3,
    Page4,
    Page5,
    Page6
  },
  methods: {
    playSound() {
      sound.play();
    },
  },
  created() {
    this.playSound();
  },
  data() {
    return {
      componentNames: ['Page1', 'Page2', 'Page3', 'Page4', 'Page5', 'Page6']
    }
  }
}
</script>

<style>
  * {
    border: 0px;
    padding: 0px;
  }
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
  }
  .carousel__item {
    top: 0;
    /* height: 100vh; */
    width: 100%;
    background-color: black;
    color:  var(--vc-clr-white);
    font-size: 20px;
    border-radius: 8px;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .carousel__slide {
    background: black;
    display: inline;
    height: auto;
  }

  .carousel__prev {
    margin-left: 20px;
    background-color: rgba(0, 0, 0, 0);
    position: fixed;
  }

  .carousel__next {
    margin-right: 20px;
    background-color:rgba(0, 0, 0, 0);;
    position: fixed;
  }


</style>
