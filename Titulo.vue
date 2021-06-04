<template>
    <h1> {{texto}}</h1>
</template>

<script>

export default {
    name: 'Titulo', 
    props: {
        texto: String // Esto es el props que le podemos mandar a nuestro template para que a su ves lo mande a llamar a App.vue
    }
}
</script>

<style scoped>

    h1{
        font-family: 'Times New Roman', Times, serif;
        color: rgba(211, 144, 19, 0.781);
      } 
</style>