<script setup>

import { defineEmits } from 'vue';

const emits = defineEmits(['selectOption'])
const selectOption = (isColor) => {
  emits("selectOption", isColor) 
}


</script>


<template>
    <v-navigation-drawer
      expand-on-hover
      rail
      width="100%"
    >

      <v-list>
        <v-list-item
          prepend-avatar="https://avatars.githubusercontent.com/u/69128509"
          title="Mateus Merçon"
          subtitle="mateusmercon@gmail.com"
        />
      </v-list>

      <v-divider/>

      <v-list density="default" nav>
        <v-list-item 
          prepend-icon="mdi-image" 
          title="Colored Images" 
          value="colored-images"
          @click="selectOption(true)"
        />

        <v-list-item 
          prepend-icon="mdi-account-multiple" 
          title="Gray Images" 
          value="gray-images"
          @click="selectOption(false)"
        />
      </v-list>

    </v-navigation-drawer>
</template>


<style lang="scss" scoped>

</style>