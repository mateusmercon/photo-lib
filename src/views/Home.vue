<script setup>

import SideBar from '../components/SideBar.vue';
import ImageGrid from '../components/ImageGrid.vue';
import { ref } from 'vue';

const isWithColor = ref(true)
const onSelectOption = (isColor) => {
  isWithColor.value = isColor
}

</script>


<template>

  <v-app>

    <SideBar @select-option="onSelectOption"/>

    <v-main>
      <ImageGrid :isWithColor="isWithColor"/>
    </v-main>

  </v-app>

</template>





