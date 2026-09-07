<script setup>
import { ref } from 'vue'

const message = ref("Choose your favourite fruit")
const fruits = ref(["apple", "orange", "peach"])
</script>

<template>
  <div>{{ message }}</div>

  <label>
    <input type="radio" name="fruit"> {{ fruits[0] }}
    <input type="radio" name="fruit"> {{ fruits[1] }}
    <input type="radio" name="fruit"> {{ fruits[2] }}
  </label>
</template>
