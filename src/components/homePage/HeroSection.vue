<template>
  <section
    class="bg-cover relative h-screen"
    :style="{ backgroundImage: `url(${bgImage})` }"
  >
    <div class="absolute inset-0 bg-black opacity-25"></div>
    <div
      class="relative flex items-center justify-center h-full text-center text-white px-4"
    >
      <div class="w-full md:w-3/5">
        <h1 class="text-4xl md:text-5xl font-bold mb-4">
          Fast & Easy Way To Hire A Car
        </h1>
        <p class="text-md md:text-xl mb-6">
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Minima
          adipisci debitis odit. Veniam recusandae labore, non harum
          voluptatibus.
        </p>
        <h2 class="text-2xl font-semibold">Easy steps for renting a car</h2>
      </div>
    </div>
  </section>
</template>

<script setup>
import bgImage from "../../assets/images/bg_1.jpg";
</script>

<style>
</style>