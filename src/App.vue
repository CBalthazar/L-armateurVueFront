<script setup>
import AllPageHeader from '@components/AllPageHeader.vue'
import { ref, watch } from 'vue'

const searchText = ref('')

watch(searchText, (val, oldval) => {
  console.log(`${oldval} => ${val}`)
})
</script>

<template>
  <AllPageHeader v-model="searchText"> Yahallo ! </AllPageHeader>
  <main>
    <section class="carroussel">a</section>
    <section class="description">b</section>
    <section class="other-links">c</section>
  </main>
  <footer>
    <p>footer</p>
  </footer>
</template>

<style scoped>
main {
  background-color: rosybrown;
  flex-grow: 1;
  display: flex;
  flex-direction: column;
}

section:nth-child(1) {
  background-color: #ffcd91;
  flex-grow: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

section:nth-child(2) {
  background-color: #ffb55e;
  flex-grow: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

section:nth-child(3) {
  background-color: #ff9e2b;
  flex-grow: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>
