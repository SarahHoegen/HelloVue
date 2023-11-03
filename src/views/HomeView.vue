<script setup>
import { Alert } from 'bootstrap';
import { ref , onMounted } from 'vue'
import Modal from "@/components/Modal.vue"

const rawHtml = '<span style="color: red">Este é um texto em vermelho</span>'
const contador = ref(0)
const openModal = ref(false)


function incrementarContador() {
    contador.value++
}
function decrementarContador() {
    if (contador.value > 0) {
      contador.value--
    }
 }
function zerarContador() {
    showModal();
    contador.value = 0
}

function showModal() {
    openModal.value = true;
}

</script>

<template>
    <font-awesome-icon :icon="['fas', 'house']" /><p>Botões funcionais</p>
    <button @click="incrementarContador">Incrementar</button>
    <button @click="decrementarContador">Decrementar</button>
    <button @click="zerarContador">Zerar valor</button><br>
    <span>Valor do contador é: {{ contador }}</span>
    <br>
    <p>Usando interpolação de textos: {{rawHtml}}</p>
    <p>Usando v-html: <span v-html="rawHtml"></span></p>

    <Modal :openModal="openModal" @close-modal="openModal = false" />

</template>
  
  <style scoped>
  button {
    border-radius: 10px;
    margin-right: 2%;
    background-color:#93cfb8;
    font-weight: bold;
  }
  </style>