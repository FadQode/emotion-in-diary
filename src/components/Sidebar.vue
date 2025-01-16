<template>
    <div
      class="fixed top-0 left-0 h-full bg-gray-800 text-white shadow-lg z-40 w-64"
    >
      <div class="flex justify-between items-center p-4">
        <h2 class="text-lg font-bold">Menu</h2>
        <button @click="closeSidebar" class="p-2 rounded-md hover:bg-gray-700">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-6 w-6 text-gray-400"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M6 18L18 6M6 6l12 12"
            />
          </svg>
        </button>
      </div>
      <nav class="mt-4">
        <ul>
          <li>
            <router-link
              to="/riwayat"
              class="block px-4 py-2 hover:bg-gray-700"
            >
              Riwayat
            </router-link>
          </li>
          <li>
            <router-link
              to="/jurnal"
              class="block px-4 py-2 hover:bg-gray-700"
            >
              Jurnal
            </router-link>
          </li>
        </ul>
      </nav>
    </div>
  </template>
  
  <script>
  export default {
    name: "Sidebar",
    methods: {
      closeSidebar() {
        this.$emit("close-sidebar");
      },
    },
  };
  </script>
  