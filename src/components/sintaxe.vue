<script setup>
    const numero = 1
    const ok = true
    const mensagem = 'programar'
    const url = 'https://vuejs.org/'
</script>

<template>
  {{ numero + 1 }}
  {{ ok ? 'Sim' : 'Não' }}
  {{ mensagem.split('').reverse().join('') }}
  <br>
    <a :href="url">Mais informações...</a>
</template>