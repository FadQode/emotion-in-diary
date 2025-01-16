<template>
    <div class="flex flex-col h-screen">
      <!-- Navbar -->
      <nav class="bg-blue-600 text-white px-4 py-3 flex justify-between items-center shadow-md">
        <!-- Sidebar Toggle Button -->
        <button
          @click="toggleSidebar"
          class="p-2 rounded-md hover:bg-blue-500 focus:ring focus:ring-blue-300"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-6 w-6"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7" />
          </svg>
        </button>
  
        <!-- Logo and Navigation -->
        <div class="flex items-center space-x-6">
          <div class="text-xl font-bold">MyApp</div>
          <ul class="hidden md:flex space-x-4">
            <li>
              <RouterLink to="/riwayat" class="hover:text-gray-200">
                Riwayat
              </RouterLink>
            </li>
            <li>
              <RouterLink to="/jurnal" class="hover:text-gray-200">
                Jurnal
              </RouterLink>
            </li>
          </ul>
        </div>
  
        <!-- Profile -->
        <div class="relative">
          <img
            src="https://via.placeholder.com/40"
            alt="Profile"
            class="w-10 h-10 rounded-full cursor-pointer"
          />
        </div>
      </nav>
  
      <!-- Sidebar -->
      <div
        :class="[
          isSidebarOpen ? 'translate-x-0' : '-translate-x-full',
          'fixed top-0 left-0 w-64 h-full bg-gray-800 text-white shadow-lg transform transition-transform duration-300 z-50',
        ]"
      >
        <button
          @click="toggleSidebar"
          class="absolute top-4 right-4 p-2 text-gray-400 hover:text-white"
        >
          ✕
        </button>
        <h2 class="text-lg font-bold p-4">Menu</h2>
        <ul class="space-y-2 p-4">
          <li>
            <RouterLink
              to="/riwayat"
              class="block py-2 px-3 rounded hover:bg-gray-700"
            >
              Riwayat
            </RouterLink>
          </li>
          <li>
            <RouterLink
              to="/jurnal"
              class="block py-2 px-3 rounded hover:bg-gray-700"
            >
              Jurnal
            </RouterLink>
          </li>
        </ul>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref } from "vue";
  
  // Sidebar toggle state
  const isSidebarOpen = ref(false);
  
  // Function to toggle sidebar
  const toggleSidebar = () => {
    isSidebarOpen.value = !isSidebarOpen.value;
  };
  </script>
  
  <style scoped>
  /* Optional: Custom styling for smoother transitions */
  </style>
  