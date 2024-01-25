<script setup lang="ts">
import { ref } from 'vue';

const value = ref(0)

const returnValue = () => {
  value.value++
  return value.value
}

</script>

<template>
  <button 
  v-on:click="$emit('test', returnValue())"
  >
  {{ value }}
  </button>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
