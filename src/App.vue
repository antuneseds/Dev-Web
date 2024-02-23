<script setup>

import { ref } from 'vue'

const contador = ref(0)

function soma() {
  contador.value++
}

function decrementar() {
  if (contador.value > 0) contador.value--
}

function resetar() {
  contador.value = 0
}

</script>

<template>
  <button @click="soma">+</button>
  <button @click="decrementar">-</button>
  <button @click="resetar">0</button>
  <p>Valor do contador: {{ contador }}</p>
</template>

<style scoped>
  button {
    font-weight: bold;
    background-color: pink;
    color: black;
    padding: 10px;
  }
</style>
