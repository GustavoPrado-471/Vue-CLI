<template>
<div id="app">
  <img alt="Vue logo" src="./assets/logo.png">
  <!-- Para mandar a llamar nuestro componente, usamos una etiqueta o pseudo etiqueta--> 
  <Titulo texto="DINAMIC BROXEL"></Titulo>
  <Cuenta />
</div>
</template>

<script>
import Titulo from './components/Titulo.vue'
import Cuenta from './components/Cuenta.vue' 

//import HelloWorld from './components/HelloWorld.vue' //De esta forma podemos importar los componentes que vamos a usar

export default {
  name: 'App',
  components: {
    Titulo, Cuenta
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
