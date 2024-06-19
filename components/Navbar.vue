<script setup>
import { ref, watch } from "vue";

const open = ref(false);

watch(open, (newValue) => {
  if (newValue) {
    document.body.classList.add("overflow-hidden");
  } else {
    document.body.classList.remove("overflow-hidden");
  }
});
</script>
<template>
  <nav>
    <div class="container xl:max-w-[1320px] mx-auto px-5 my-3">
      <div class="flex flex-wrap items-center justify-between">
        <a href="#" class="text-5xl font-bold text-cyan-600">Nuxt Js</a>
        <div @click="open = !open" class="block lg:hidden relative z-50">
          <div
            class="w-8 h-1 bg-black rounded mb-1 transition-all duration-300 ease-linear"
            :class="{ 'translate-y-[11px] -rotate-45': open, '': !open }"
          ></div>
          <div
            class="w-8 h-1 bg-black rounded mb-1 transition-all duration-300 ease-linear"
            :class="{ hidden: open, '': !open }"
          ></div>
          <div
            class="w-8 h-1 bg-black rounded transition-all duration-300 ease-linear"
            :class="{ 'translate-y-[50%] rotate-45': open, '': !open }"
          ></div>
        </div>
        <ul
          class="lg:flex items-center lg:flex-row flex-col gap-5 max-lg:z-40 max-lg:fixed max-lg:h-full max-lg:left-0 max-lg:w-full max-lg:bg-white max-lg:justify-center transition-all ease-linear duration-300 flex"
          :class="{ 'max-lg:top-0': open, 'max-lg:top-[-100%]': !open }"
        >
          <li @click="open = !open">
            <a href="#home" class="text-lg font-medium text-cyan-950">Home</a>
          </li>
          <li @click="open = !open">
            <a href="#about" class="text-lg font-medium text-cyan-950">About Us</a>
          </li>
          <li @click="open = !open">
            <a href="#portfolio" class="text-lg font-medium text-cyan-950"
              >Roadmap</a
            >
          </li>
          <li @click="open = !open">
            <a href="#contact" class="text-lg font-medium text-cyan-950"
              >Faqs</a
            >
          </li>
          <li @click="open = !open">
            <a href="#product" class="text-lg font-medium text-cyan-950"
              >Contact</a
            >
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>
