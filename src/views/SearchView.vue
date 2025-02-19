<script setup>
import AllPageHeader from '@components/AllPageHeader.vue'
import { ref } from 'vue'
const searchText = ref('')
</script>

<template>
  <AllPageHeader v-model="searchText"> Yahallo ! </AllPageHeader>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
