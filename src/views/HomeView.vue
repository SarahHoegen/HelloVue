<script>
export default {
  data() {
    return {
      contador: 0
    }
  },
  methods: {
    incrementarContador() {
      this.contador++
    },
    decrementarContador() {
        if (this.contador > 0) {
            this.contador--
        }
    },
    ZerarContador() {
        this.contador = 0
        
    }
  },
  mounted() {
    console.log(`O valor inicial do contador é ${this.contador}.`)
  }
}
</script>

<template>
    <p>Botões funcionais</p>
    <button @click="incrementarContador">Incrementar</button>
    <button @click="decrementarContador">Decrementar</button> <br><br>
    <button @click="ZerarContador">Zerar valor</button>
    <p>Valor do contador é: {{ contador }}</p>
</template>
  
  <style scoped>
  button {
    border-radius: 10px;
    margin-right: 2%;
    background-color:#93cfb8;
    font-weight: bold;
  }
  </style>