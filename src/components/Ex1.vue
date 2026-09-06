<script setup>
import { ref } from 'vue'

const message = ref("Choose your favourite fruit")

// Challenge: Single array storing all fruits
const fruits = ref(["apple", "orange", "peach"])
</script>

<template>
  {{ message }}

  <!-- Loop through the array directly -->
  <label v-for="fruit in fruits" :key="fruit">
    <input type="radio" name="fruit"> {{ fruit }}
  </label>
</template>

<style scoped>
</style>
