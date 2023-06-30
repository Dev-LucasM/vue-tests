<template>
  <div>
    <Header />
    <PrimeiroComponente />
    <p class="paragrafo-pai">Paragrafo pai {{ testando }}</p>
    <LifeCycle />
    <Pessoa />
  </div>
</template>

<script>
  import PrimeiroComponente from './components/PrimeiroComponente.vue'
  import LifeCycle from './components/LifeCycle.vue';
  import Header from './components/Header.vue'
  import Pessoa from './components/Pessoa.vue';

  export default {
    name: 'App',
    components: {
      PrimeiroComponente,
      LifeCycle,
      Pessoa,
      Header
    },
    data() {
      return {
        testando:  'Teste'
      }
    },
  }
</script>

<style>
  body {
    background-color: #333;
    color: #fff;
  }

  a {
    color: red;
  }

  .teste {
    background-color: #000;
  }
</style>