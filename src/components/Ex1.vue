<script setup>
import { ref } from 'vue'

const message = ref("Choose your favourite fruit")
const fruits = ref(["apple", "orange", "peach"])
</script>

<template>
  <div>{{ message }}</div>

  <label v-for="fruit in fruits" :key="fruit">
    <input type="radio" name="fruit"> {{ fruit }}
  </label>
</template>
