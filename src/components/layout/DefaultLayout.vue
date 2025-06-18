<template>
  <div class="min-h-screen flex flex-col relative">
    <!-- Header -->
    <PageHeader />

    <!-- Main content -->
    <main class="flex-grow">
      <router-view></router-view>
    </main>

    <!-- Footer -->
    <PageFooter />
  </div>
</template>

<script>
import PageFooter from "./PageFooter.vue";
import PageHeader from "./PageHeader.vue";

export default {
  components: {
    PageFooter,
    PageHeader,
  },
};
</script>

<style>
</style>