<template>
  <div>
    <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
    <p v-else>Estou em busca de novos desafios</p>
    <p>Utilizo as seguintes tecnologias:</p>
    <ul>
      <li>JavaScript</li>
      <li>Phyton</li>
      <li>PHP</li>
    </ul>
    <div>
      <button @click="showEmail">{{ textoBotao }}</button>
    </div>
    <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
    <p class="teste">Para acessar meu portfólio <a v-bind:href="meu_link" target="_blank">basta clicar aqui</a></p>
    <Picture />
  </div>
</template>

<script>
  import Picture from './Picture.vue'

  export default {
    name: 'Info',
    data() {
      return {
        esta_trabalhando: false,
        mostrar_email: false,
        email: "lucas@email.com",
        meu_link: 'https://google.com',
        textoBotao: 'Mostrar e-mail'
      }
    },
    components: {
      Picture
    },
    methods: {
      showEmail() {
        this.mostrar_email = !this.mostrar_email
        if(!this.mostrar_email) {
          this.textoBotao = "Mostrar e-mail"
        } else {
          this.textoBotao = "Ocultar e-mail"
        }
      }
    }
  }
</script>

<style>
  .paragrafo-pai {
    color: red;
  }
</style>