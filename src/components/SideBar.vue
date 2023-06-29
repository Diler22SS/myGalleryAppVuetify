<script setup>
  import { defineEmits } from "vue"

  const emits = defineEmits(['selectPortrait'])

  const selectPortrait = (size) => {
    emits("selectPortrait", size)
  }
</script>

<template>
  <v-navigation-drawer
  expand-on-hover=""
  >
    <v-list>
        <v-list-item
        title="Gallery"
        ></v-list-item>
    </v-list>

    <v-divider></v-divider>

    <v-list density="compact" nav>
      <v-list-item 
        prepend-icon="mdi-crop-portrait" 
        title="Portrait"
        color="blue" 
        value="portrait"
        @click="selectPortrait(true)"
      ></v-list-item>
      <v-list-item 
        prepend-icon="mdi-crop-square" 
        title="Square" 
        value="square"
        color="red"
        @click="selectPortrait(false)"
      ></v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>