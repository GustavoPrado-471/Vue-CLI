<template>

  <button @click="accion" :disabled="desactivar"> {{texto2}} </button> 

</template>

<script>
export default {
    props:{
        texto2: String, 
        desactivar: Boolean
    }, 
    methods: {
        accion(){ 
            this.$emit('accion')
        }
    },
}
</script>

<style>

</style>