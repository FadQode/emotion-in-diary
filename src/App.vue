<script setup>
import Navbar from './components/Navbar.vue';
</script>

<template>
  <div id="app" class="flex flex-col h-screen">
    <!-- Navbar Component -->
    <Navbar />

    <!-- Main Content -->
    <main class="flex-grow bg-gray-100 p-6">
      <router-view />
    </main>
  </div>
</template>

<style>
/* Optional: Global styles for the app */
</style>
s