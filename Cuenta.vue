<template>
  <h2>Tipo de cuenta: {{cuenta}}</h2>
  <h2> Saldo disponible: {{saldo}}</h2>

  <h3> Estado de la cuenta: {{estado ? 'Activa' : 'Desactivda'}}</h3>
   <div v-for="(servicio, index) in servicios" :key="index">
           Tipo de cuenta: {{servicio}}
   </div> 
   <AccionSaldo @accion="agregarSaldo" texto2="Aumentar Saldo" > </AccionSaldo> 
   <AccionSaldo @accion="disminuirSaldo" 
                :desactivar="desactivar"
                texto2="Disminuir Saldo" ></AccionSaldo>

</template>

<script>

import AccionSaldo from './AccionSaldo'

export default {

    components:{
        AccionSaldo,
    }, 
    data() {
        return {
            saldo: 1000, 
            cuenta: "Visa",
            estado: false, 
            servicios: ['Banamex', 'ScotiaBank', 'BBVA', 'Santander'],
            desactivar: false
            
        }
    },
    methods: {
        agregarSaldo(){ 
            this.saldo = this.saldo + 100;
            this.desactivar = false
        }, 

        disminuirSaldo (){ 
            if (this.saldo === 0){ 

                this.desactivar = true
                alert('Eres un pobre diablo')
                return
            }
            this.saldo = this.saldo - 100; 
        }
    },
}
</script>



<style scoped>
h2{ 
    font-family: 'Times New Roman', Times, serif;
    color: rgba(24, 134, 110, 0.74);
}
</style>