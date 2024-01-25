<script setup lang="ts">
import { ref } from 'vue';
import TestAPI from './components/ComponentChild.vue'

const count = ref(0)
</script>

<template>
  count: {{ count }}
  <br/>
  <TestAPI 
    v-on:test="count = $event"
    />
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
