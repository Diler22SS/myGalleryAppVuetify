<script setup>
  import {defineProps} from "vue"

  const props = defineProps(["isPortrait"])
</script>


<template>
  <v-card class="mx-5 my-5 pa-3">
    <v-row>
      <v-col
        v-for="n in 15"
        :key="n"
        cols="12"
        sm="6"
        md="4"
      >
        <v-card>
          <v-img
            :src="`https://lipsum.app/id/${n+10}/${props.isPortrait ? '1080x1920' : '600x600'}`"
            aspect-ratio="1"
            cover
            class="bg-grey-lighten-2"
          >
            <template v-slot:placeholder>
              <v-row
                class="fill-height ma-0"
                align="center"
                justify="center"
              >
                <v-progress-circular
                  indeterminate
                  color="grey-lighten-5"
                ></v-progress-circular>
              </v-row>
            </template>
          </v-img>
        </v-card>
      </v-col>
    </v-row>
  </v-card>
</template>