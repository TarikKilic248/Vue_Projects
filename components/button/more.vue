<script setup lang="ts">
import { useTmdbStore } from '~/stores/tmdb'

const tmdbStore = useTmdbStore()
</script>

<template>
  <div v-if="tmdbStore.mediaList" class="flex w-full justify-center">
    <button
      class="cursor-pointer flex justify-between dark:bg-gray-800 bg-slate-300 px-3 py-2 rounded-full text-black dark:text-white tracking-wider shadow-xl dark:hover:bg-gray-900 hover:bg-gray-400 hover:scale-105 duration-500 hover:ring-1 font-mono w-[150px]"
      @click="tmdbStore.loadMoreMediaList()"
    >
      Add More
      <svg
        xmlns="http://www.w3.org/2000/svg"
        fill="none"
        viewBox="0 0 24 24"
        stroke-width="2"
        stroke="currentColor"
        class="w-5 h-5 animate-bounce"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          d="M19.5 13.5 12 21m0 0-7.5-7.5M12 21V3"
        />
      </svg>
    </button>
  </div>
</template>
