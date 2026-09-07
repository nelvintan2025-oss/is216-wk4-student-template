<script setup>
    import { ref } from 'vue'

    // Add code here
    const me = ref("/assets/me.png");
    const obj = ref({
      src: "/assets/wad.png",
      alt: "hello",
      width: 200,
      height: 200
    })
</script>

<template>
    <!-- Add code here -->
     <img :src="me">
     <img v-bind="obj">
</template>


