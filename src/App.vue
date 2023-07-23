<script setup>

import { ref } from 'vue';

const fullImage = ref('https://images.unsplash.com/photo-1689427147115-ee9ea359b658?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1024&q=60');

const images = [
  {
    thumb: "https://images.unsplash.com/photo-1689427147115-ee9ea359b658?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=300&q=60",
    full: "https://images.unsplash.com/photo-1689427147115-ee9ea359b658?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1024&q=60"
  },
  {
    thumb: "https://images.unsplash.com/photo-1689604926022-747e73d6d021?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=300&q=60",
    full: "https://images.unsplash.com/photo-1689604926022-747e73d6d021?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1024&q=60"
  },
  {
    thumb: "https://images.unsplash.com/photo-1689101298178-4db5b7a8c49f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=300&q=60",
    full: "https://images.unsplash.com/photo-1689101298178-4db5b7a8c49f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1024&q=60"
  },
  {
    thumb: "https://images.unsplash.com/photo-1688153454230-a3a4d253df0a?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=300&q=60",
    full: "https://images.unsplash.com/photo-1688153454230-a3a4d253df0a?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1024&q=60"
  }
]

const setfullImage = (image) => {
  fullImage.value = image.full
}
</script>

<template>
  <section class="container mx-auto flex items-center flex-col">
    <h1 class="text-center text-2xl py-10">Events & Reactivity</h1>
    <div class="">
      <div class="mt-10">
        <img class="cursor-pointer w-full" :src="fullImage" alt="">
      </div>
      <div class="flex space-x-2">
        <img @click="setfullImage(image)" class="cursor-pointer" v-for="image in images" :key="image.thumb"
             :src="image.thumb">
      </div>

    </div>
  </section>
</template>

<style scoped></style>
