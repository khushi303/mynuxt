<template>
  <div class="overflow-hidden container xl:max-w-[1320px] mx-auto px-5 py-10">
    <h1 class="text-5xl font-bold text-center">About Us</h1>
    <swiper
      :pagination="{
        dynamicBullets: true,
        clickable: true,
      }"
      :breakpoints="{
        '0': {
          slidesPerView: 2,
          spaceBetween: 20,
        },
        '640': {
          slidesPerView: 3,
          spaceBetween: 40,
        },
        '768': {
          slidesPerView: 4,
          spaceBetween: 50,
        },
      }"
      :loop="true"
      :modules="modules"
      :space-between="50"
      @swiper="onSwiper"
      @slideChange="onSlideChange"
      class="pb-10"
    >
      <swiper-slide class="w-full py-10">
        <div
          class="w-full h-full bg-slate-500 py-10 mx-auto flex items-center justify-center"
        >
          <p class="text-white text-center text-2xl">Hiii</p>
        </div>
      </swiper-slide>
      <swiper-slide class="w-full py-10">
        <div
          class="w-full h-full bg-slate-500 py-10 mx-auto flex items-center justify-center"
        >
          <p class="text-white text-center text-2xl">Hiii</p>
        </div>
      </swiper-slide>
      <swiper-slide class="w-full py-10">
        <div
          class="w-full h-full bg-slate-500 py-10 mx-auto flex items-center justify-center"
        >
          <p class="text-white text-center text-2xl">Hiii</p>
        </div>
      </swiper-slide>
      <swiper-slide class="w-full py-10">
        <div
          class="w-full h-full bg-slate-500 py-10 mx-auto flex items-center justify-center"
        >
          <p class="text-white text-center text-2xl">Hiii</p>
        </div>
      </swiper-slide>
      <swiper-slide class="w-full py-10">
        <div
          class="w-full h-full bg-slate-500 py-10 mx-auto flex items-center justify-center"
        >
          <p class="text-white text-center text-2xl">Hiii</p>
        </div>
      </swiper-slide>
      <swiper-slide class="w-full py-10">
        <div
          class="w-full h-full bg-slate-500 py-10 mx-auto flex items-center justify-center"
        >
          <p class="text-white text-center text-2xl">Hiii</p>
        </div>
      </swiper-slide>
      <swiper-slide class="w-full py-10">
        <div
          class="w-full h-full bg-slate-500 py-10 mx-auto flex items-center justify-center"
        >
          <p class="text-white text-center text-2xl">Hiii</p>
        </div>
      </swiper-slide>
      <swiper-slide class="w-full py-10">
        <div
          class="w-full h-full bg-slate-500 py-10 mx-auto flex items-center justify-center"
        >
          <p class="text-white text-center text-2xl">Hiii</p>
        </div>
      </swiper-slide>
      <swiper-slide class="w-full py-10">
        <div
          class="w-full h-full bg-slate-500 py-10 mx-auto flex items-center justify-center"
        >
          <p class="text-white text-center text-2xl">Hiii</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

import "swiper/css/pagination";

// import required modules
import { Pagination } from "swiper/modules";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    const onSwiper = (swiper) => {
      console.log(swiper);
    };
    const onSlideChange = () => {
      console.log("slide change");
    };
    return {
      onSwiper,
      onSlideChange,
      modules: [Pagination],
    };
  },
};
</script>
