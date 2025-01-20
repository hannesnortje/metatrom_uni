<template>
  <div class="default-layout min-h-screen flex flex-col">
    <header class="bg-gray-100 p-4">
      <!-- Header content -->
      <h1 class="text-2xl font-bold">{{ title }}</h1>
    </header>
    <main class="flex-grow p-4">
      <slot />
      <!-- This is where nested routes or content will be rendered -->
    </main>
    <footer class="bg-gray-100 p-4 text-center">
      <!-- Footer content -->
      <p>© {{ currentYear }} My Company</p>
    </footer>
  </div>
</template>

<script setup lang="ts">
import { ref, computed } from 'vue'

const title = ref('My App')
const currentYear = computed(() => new Date().getFullYear())
</script>

<style scoped>
/* No additional CSS needed if using Tailwind classes */
</style>
