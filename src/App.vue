<script setup>
import {ref} from "vue";
const counter = ref(0); 
 
const increment =() => {
  counter.value++;
}
const decrement =() => {
  counter.value--;
}
</script>

<template>
  <header>

  </header>

  <main>
   <h1>Counter: {{ counter }}</h1>
   <button @click="increment">Increment</button>
   <button v-on:click="decrement">Decrement</button>
  </main>
</template>

<style scoped>

</style>
