<script setup>
import { ref } from 'vue'

// Part 1: Background toggle state
const id = ref('demo')
const blueBox = ref(true)
const blueBtn = ref(true)

// Part 2: Text color toggle state
const id2 = ref('demo2')
const activeColor = ref('red')
const redBtn = ref(false)

// Methods
function changeColor() {
  blueBox.value = !blueBox.value
  blueBtn.value = !blueBtn.value
}

function changeTextColor() {
  if (activeColor.value === 'red') {
    activeColor.value = 'blue'
    redBtn.value = true
  } else {
    activeColor.value = 'red'
    redBtn.value = false
  }
}
</script>

<template>
  <!-- Part 1: Background Color Binding -->
  <div id="part1">
    <div :id="id" :class="{ blueBox: blueBox, redBox: !blueBox }">
      div ID : {{ id }}
    </div>

    <button
      type="button"
      :class="[blueBtn ? 'btn-primary' : 'btn-danger']"
      @click="changeColor"
    >
      Change Color
    </button>
  </div>

  <br>

  <!-- Part 2: Inline Style Binding -->
  <div id="part2">
    <div :id="id2" :style="{ color: activeColor }">
      div ID : {{ id2 }}
    </div>

    <button
      type="button"
      :class="[redBtn ? 'btn-primary' : 'btn-danger']"
      @click="changeTextColor"
    >
      Change Text Color
    </button>
  </div>
</template>

<style scoped>
.redBox {
  background-color: red;
}
.blueBox {
  background-color: blue;
}
.btn-primary {
  background-color: blue;
  color: white;
}
.btn-danger {
  background-color: red;
  color: white;
}
#demo {
  color: white;
}
</style>
