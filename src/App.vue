<script setup>
  import SideBar from "./components/SideBar.vue"
  import ImageGallery from "./components/ImageGallery.vue"
  import {ref} from "vue"

  const isPortrait = ref(true)
  const onSelectPortrait = (size) => {
    isPortrait.value = size;
  }
</script>


<template>
  <v-app>
    <side-bar @selectPortrait="onSelectPortrait"/>
    <v-main>
      <image-gallery :isPortrait="isPortrait"/>
    </v-main>
  </v-app>
</template>
