<script setup>
import { ref, onMounted } from 'vue'

const contador = ref(0)

function incrementarContador() {
  contador.value++
}

function decrementarContador() {
  if (contador.value > 0){
    contador.value-- 
  }
}

function resetarContador() {
  contador.value = 0
}

onMounted(() => {
  console.log(`O valor inicial do contador é ${contador.value}.`)
})
</script>

<template>
  <button @click="incrementarContador">Incrementar</button>
  <button @click="decrementarContador">Decrementar</button>
  <p>Valor do contador é: {{ contador }}</p>
  <button @click="resetarContador">Resetar</button>
</template>

<style scoped>
button {
  font-weight: bold;
}
</style>