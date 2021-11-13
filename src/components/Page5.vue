<template>
  <Carousel :autoplay="50000" :wrap-around="true">
    <Slide v-for="slide in 5" :key="slide">
      <div class="carousel__item"><img :src="`../assets/pg5luz${slide}.jpg`"></div>
     
    </Slide>

    <template #addons>
    </template>
  </Carousel>
</template>

<script>
import { defineComponent } from 'vue'
import { Carousel, Slide } from 'vue3-carousel';

import 'vue3-carousel/dist/carousel.css';

export default defineComponent({
  name: 'Autoplay',
  components: {
    Carousel,
    Slide,
  },
  data() {
      return{
          slidesluz: ["../assets/pg5luz1.jpg", "../assets/pg5luz2.jpg", "../assets/pg5luz3.jpg", "../assets/pg5luz4.jpg", "../assets/pg5luz5.jpg"]
      }
  }
});
</script>