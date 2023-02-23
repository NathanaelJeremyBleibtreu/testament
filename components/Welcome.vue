<template>
  <client-only>
    <h1>TESTAMENT</h1>
    <h2>An interactive story</h2>
    <p>{{intro}}</p>
    <button @click="erase()">Effacer</button>
  </client-only>
</template>

<script setup>
import { ref } from 'vue'

export default {
  setup(){
    // reactive state
    const intro = ref("Salut les kids")
    
    // functions that mutate state and trigger updates
    function erase() {
      intro.value = "erased";
    }
    
    return {
      erase, intro
    }
    
  },

  // lifecycle hooks
  mounted() {
    console.log(`The initial intro is ${intro.value}.`)
  }

}
</script>


<style>

</style>