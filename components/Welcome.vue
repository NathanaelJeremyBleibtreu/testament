<template>
  <h1>TESTAMENT</h1>
  <h2>An interactive story</h2>
  <p>{{intro}}</p>
  <button @click="erase()">Effacer</button>
</template>

<script setup>
import { ref, onMounted } from 'vue'

// reactive state
const intro = ref("Salut les kids")

// functions that mutate state and trigger updates
function erase() {
  intro.value = "erased";
}

// lifecycle hooks
onMounted(() => {
  console.log(`The initial intro is ${intro.value}.`)
})
</script>


<style>

</style>