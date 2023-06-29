<template>
  <div>
    <PrimeiroComponente />
    <p>Olá {{ testando }}</p>
  </div>
</template>

<script>
  import PrimeiroComponente from './components/PrimeiroComponente.vue'

  export default {
    name: 'App',
    components: {
      PrimeiroComponente
    },
    data() {
      return {
        testando:  'Teste'
      }
    },
  }
</script>
