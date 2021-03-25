<template>
  <input
    type="text"
    placeholder="searching for .. "
    class="text-center container block mx-auto rounded-full mt-8 p-2 text-2xl focus:ring-4 focus:ring-green-600 focus:ring-opacity-50"
    v-model="searchItem"
    @change="getGifs"
  />
</template>

<script setup>
import { searchItem, getGifs } from "../helpers/useGifs"
</script>
