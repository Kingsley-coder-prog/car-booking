<template>
  <router-link to="/">
    <h1 class="uppercase text-xl font-bold cursor-pointer">
      <span :class="carClass">car</span>
      <span class="text-green-500">book</span>
    </h1>
  </router-link>
</template>

<script>
import { computed, onBeforeUnmount, onMounted, ref } from "vue";
export default {
  setup() {
    const isScrolled = ref(false);
    const isMobile = ref(window.innerWidth < 760);

    const handleScroll = () => {
      isScrolled.value = window.scrollY > 50;
    };

    onMounted(() => {
      window.addEventListener("scroll", handleScroll);
    });

    onBeforeUnmount(() => {
      window.removeEventListener("scroll", handleScroll);
    });

    const carClass = computed(() => {
      if (isMobile.value) return "text-black";
      return isScrolled.value ? "text-black" : "text-white";
    });

    return {
      carClass,
    };
  },
};
</script>

<style>
</style>