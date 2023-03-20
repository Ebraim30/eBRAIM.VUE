<script setup>

import { ref, onMounted } from 'vue'

const contador = ref(0)
const contador2 = ref(0)

function incrementarContador() {
  contador.value++
}
function decrementarContador() {
  contador.value--
}
function incrementarContador2() {
  contador2.value++
}
function decrementarContador2() {
  contador2.value--
}
onMounted(() => {
  console.log(`O valor inicial do contador é ${contador.value}.`)
}) 
    
</script>

<template>
    <div>
    <div> <button @click="incrementarContador">+</button>
    <button @click="decrementarContador">-</button>
    <p>Valor do contador é: {{ contador }}</p>
     </div>  
     
     <div>
        <p>+</p>
     </div>

     
    <div><button @click="incrementarContador2">+</button>
    <button @click="decrementarContador2">-</button>
    <p>Valor do contador é: {{ contador2 }}</p>
    </div>
    </div>

    <p>resultado = {{ contador + contador2 }}</p>

</template>

<style scoped>

</style>