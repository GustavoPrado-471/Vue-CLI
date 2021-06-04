<template> 
  <div class="hello"> <!--En la parte del template podemos agregar las cosas que vamos a usar en el HTML--> 
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
export default { 
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>


<style scoped> 
h3 { /*Con ayuda de scope podemos usar los estilos de CSS de manera local*/
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
