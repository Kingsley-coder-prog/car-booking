<template>
  <section
    class="bg-cover relative h-screen"
    :style="{ backgroundImage: `url(${bgImage})` }"
  >
    <div class="absolute inset-0 bg-black opacity-25"></div>
    <div>
      <h1>Fast & Easy Way To Hire A Car</h1>
      <p>
        Lorem ipsum dolor sit amet consectetur, adipisicing elit. Minima
        adipisci debitis odit. Veniam recusandae labore, non harum voluptatibus,
        quae natus sit voluptas excepturi, culpa cumque ex quis vero molestiae!
        Earum.
      </p>
    </div>
  </section>
</template>

<script setup>
import bgImage from "../../assets/images/bg_1.jpg";
</script>

<style>
</style>