<template>
  <Search />
  <div
    class="mt-8 container mx-auto grid gap-6 grid-cols-2 md:grid-cols-3 lg:grid-cols-4 xl:grid-cols-6"
  >
    <router-link v-for="gif in gifs" :key="gif.id" :to="`/${gif.id}`">
      <img :src="gif.images.downsized.url" />
    </router-link>
  </div>
</template>
<script setup>
import { onMounted } from "vue"
import { gifs, getGifs } from "../helpers/useGifs"

onMounted(() => {
  getGifs()
})
</script>
