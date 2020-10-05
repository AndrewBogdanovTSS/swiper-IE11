<template>
  <!-- Slider main container -->
  <div class="swiper-container">
    <!-- Additional required wrapper -->
    <div class="swiper-wrapper">
      <!-- Slides -->
      <div class="swiper-slide">Slide 1</div>
      <div class="swiper-slide">Slide 2</div>
      <div class="swiper-slide">Slide 3</div>
      ...
    </div>
    <!-- If we need pagination -->
    <div class="swiper-pagination" />

    <!-- If we need navigation buttons -->
    <div class="swiper-button-prev" />
    <div class="swiper-button-next" />
  </div>
</template>

<script>
// core version + navigation, pagination modules:
import Swiper, { Navigation, Pagination } from 'swiper'

// configure Swiper to use modules
Swiper.use([Navigation, Pagination])

// import Swiper styles
import 'swiper/swiper-bundle.css'

export default {
  name: '',
  mounted() {
    new Swiper('.swiper-container', {
      // If we need pagination
      pagination: {
        el: '.swiper-pagination',
      },

      // Navigation arrows
      navigation: {
        nextEl: '.swiper-button-next',
        prevEl: '.swiper-button-prev',
      }
    })
  }
}
</script>

<style scoped>
.swiper-container {
  width: 600px;
  height: 300px;
}
.swiper-slide {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
