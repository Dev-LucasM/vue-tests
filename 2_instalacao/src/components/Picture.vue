<template>
  <img :src="avatar" :alt="descricao">
</template>

<script>
export default {
  name: 'Picture',
  data() {
    return {
      avatar: "/img/humburger-category.svg",
      descricao: "foto hamburguer"
    }
  }
}
</script>