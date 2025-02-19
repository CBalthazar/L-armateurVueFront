<script setup>
import { RouterLink } from 'vue-router'
defineProps(['modelValue'])
const emit = defineEmits(['update:modelValue'])
</script>

<template>
  <header>
    <h1>L'armateur</h1>
    <div>
      <!-- missing @change -->
      <input
        type="text"
        placeholder="Search"
        :value="modelValue"
        @keyup.enter="emit('update:modelValue', $event.target.value)"
      />
    </div>
    <nav>
      <RouterLink to="/">Explorer</RouterLink>
      <RouterLink to="/">Notes</RouterLink>
      <RouterLink to="/">Communeauté</RouterLink>
      <RouterLink to="/">Account</RouterLink>
    </nav>
  </header>
</template>

<style scoped>
header {
  display: flex;
  align-items: center;
  gap: 3em;
  background-color: #44bba4;
}

div {
  flex-grow: 1;
  height: 2em;
  display: flex;
  font-size: 1.5em;
}

div input {
  flex-grow: 1;
  padding: 0 1em;
}

div input:focus {
  border: 3px solid #555;
}

nav {
  display: flex;
  align-items: center;
  font-size: 1.5em;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  padding: 0 0.5em;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

nav a:hover {
  background-color: darken(#44bba4, 20%);
}
</style>
