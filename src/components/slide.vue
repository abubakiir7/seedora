<template>
  <div class="container ">
    <h1 class="text-4xl font-bold flex justify-center py-16">
      What out clients say
    </h1>
  </div>
  <Carousel :itemsToShow="3.95" :wrapAround="true" :transition="500" class="max-md:hidden">
    <Slide v-for="slide in 10" :key="slide">
      <div class="carousel__item max-w-[500px]">
        <div class="border border-[#EFEFEF] py-11 px-8 rounded-xl">
          <div class="flex items-center gap-6 mb-7">
            <img src="../assets/img/imgs/carousel.png" alt="" />
            <div class="text-start">
              <h3 class="text-lg font-bold">Carla Samantoes-Diego</h3>
              <span class="text-[#70737C] text-md">12.09.2021</span>
            </div>
          </div>
          <div class="flex items-center gap-1 mb-4">
            <img src="../assets/img/icons/star.svg" alt="" />
            <img src="../assets/img/icons/star.svg" alt="" />
            <img src="../assets/img/icons/star.svg" alt="" />
            <img src="../assets/img/icons/star.svg" alt="" />
            <img src="../assets/img/icons/Vector.svg" alt="" />
          </div>
          <p class="font-light text-start">
            SEEDRA Spinach Seeds - contains 600 seeds in 2 Packs and
            professional instructions created by PhD Helga George Be sure of our
            quality - the freshest batches of this season. Non-GMO, Heirloom -
            our seeds were tested and have the best germination ratings.
          </p>
        </div>
      </div>
    </Slide>
  </Carousel>
</template>

<script>
import { defineComponent } from "vue";
import { Carousel, Pagination, Slide } from "vue3-carousel";

import "vue3-carousel/dist/carousel.css";

export default defineComponent({
  name: "Autoplay",
  components: {
    Carousel,
    Slide,
    Pagination,
  },
});
</script>

<style scoped>
.carousel__slide {
  padding: 10px;
}

.carousel__viewport {
  perspective: 20000px;
}

.carousel__track {
  transform-style: preserve-3d;
}

.carousel__slide--sliding {
  transition: 0.5s;
}

.carousel__slide {
  opacity: 0.9;
  transform: rotateY(-20deg) scale(0.9);
}

.carousel__slide--active ~ .carousel__slide {
  transform: rotateY(20deg) scale(0.9);
}

.carousel__slide--prev {
  opacity: 1;
  transform: rotateY(-10deg) scale(0.95);
}

.carousel__slide--next {
  opacity: 1;
  transform: rotateY(10deg) scale(0.95);
}

.carousel__slide--active {
  opacity: 1;
  transform: rotateY(0) scale(1.1);
}
</style>
