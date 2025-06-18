<template>
  <header class="flex justify-centre px-6 z-50 fixed w-full top-0 p-2">
    <div class="flex justify-between items-centre w-full md:w-5/6 md:relative">
      <PageLogo />
      <nav class="space-x-6 p-2">
        <router-link
          v-for="link in links"
          :key="link.path"
          :to="link.path"
          :class="{ 'active-link': route.path === link.path }"
          >{{ link.name }}</router-link
        >
      </nav>
    </div>
  </header>
</template>

<script setup>
import PageLogo from "../composables/PageLogo.vue";
import { useRoute } from "vue-router";

const route = useRoute();
const isScrolled = ref(false);
const menuVisible = ref(false);

const links = [
  { name: "Home", path: "/" },
  { name: "About", path: "/about" },
  { name: "Services", path: "/services" },
  { name: "Pricing", path: "/pricing" },
  { name: "Cars", path: "/cars" },
  { name: "Blog", path: "/blog" },
  { name: "Contact", path: "/contact" },
];

const headerClass = computed(() => ({
  "sm:bg-transparent": !isScrolled.value,
  "sm:bg-white": isScrolled.value,
}));
</script>

<style>
nav a {
  color: white;
  transition: color 0.3s ease;
}

nav a.active-link {
  color: #10b981;
  font-weight: bold;
}
</style>