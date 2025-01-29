<template>
  <nav class="bg-gray-800 text-white sticky top-0">
    <div class="mx-auto flex items-center justify-between px-4 py-3">
      <!-- Brand with Logo -->
      <a href="#" class="flex items-center text-xl font-bold text-green-400">
        Movie4U
      </a>

      <!-- Hamburger Menu -->
      <button
        @click="toggleMenu"
        :class="{ open: isMenuOpen, 'bg-gray-700': isMenuOpen }"
        class="block md:hidden text-white focus:outline-none relative p-2 rounded-md transition-all duration-300 ease-in-out"
        aria-label="Toggle navigation"
      >
        <svg
          v-if="!isMenuOpen"
          class="w-6 h-6"
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M4 6h16M4 12h16m-7 6h7"
          />
        </svg>
        <svg
          v-if="isMenuOpen"
          class="w-6 h-6"
          xmlns="http://www.w3.org/2000/svg"
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

      <!-- Navigation Links -->
      <ul
        :class="{ hidden: !isMenuOpen, block: isMenuOpen }"
        class="absolute inset-x-0 top-16 bg-gray-800 space-y-2 md:space-y-0 md:flex md:static md:bg-transparent md:items-center md:space-x-6"
      >
        <li class="nav-item ml-2">
          <a
            href="#"
            class="block px-3 py-2 text-white hover:opacity-85"
          >
            Home
          </a>
        </li>
        <li class="nav-item ml-2">
          <a
            href="#"
            class="block px-3 py-2 text-white hover:opacity-85"
          >
            Chinese
          </a>
        </li>
        <li class="nav-item ml-2">
          <a
            href="#"
            class="block px-3 py-2 text-white hover:opacity-85"
          >
            Thai
          </a>
        </li>
        <li class="nav-item ml-2">
          <a
            href="#"
            class="block px-3 py-2 text-white hover:opacity-85"
          >
            Indonesia
          </a>
        </li>
        <li class="nav-item ml-2">
          <a
            href="#"
            class="block px-3 py-2 text-white hover:opacity-85"
          >
            Khmer
          </a>
        </li>
        <li class="nav-item ml-2">
          <a
            href="#"
            class="block px-3 py-2 text-white hover:opacity-85"
          >
            Contact
          </a>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script setup>
import { ref } from "vue";

// State for managing menu visibility
const isMenuOpen = ref(false);

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};
</script>

<style scoped>
/* Optional: smooth transition for the button on open */
button.open svg:nth-child(1) {
  transform: rotate(45deg);
}

button.open svg:nth-child(2) {
  transform: rotate(-45deg);
}
</style>
