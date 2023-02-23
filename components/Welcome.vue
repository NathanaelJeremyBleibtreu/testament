<template>
    <h1>TESTAMENT</h1>
    <h2>An interactive story</h2>
    <p>{{intro}}</p>
    <button @click="erase()">Effacer</button>
</template>

<script setup>
import { ref } from 'vue'

const intro = ref("Salut les kids")

// functions that mutate state and trigger updates
const erase = () => {
  intro.value = "erased";
}

</script>


<style>

</style>