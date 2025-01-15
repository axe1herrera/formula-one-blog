
<!--Composition API-->
<template>
  <h1>Hola mundo</h1>
  <p>{{contador}}</p>
  <button @click="incrementar" class="increment">Incrementar</button>
  <button @click="decrementar" class="decrement" >Decrementar</button>

</template>

<script setup>
import {ref} from 'vue';
const contador = ref(0);
const incrementar = () => {
  contador.value++;
}
const decrementar = () => {
  contador.value--;
}


</script>

<style scoped>
.increment {
  color: green;
}
.decrement {
  color: red;
}
</style>
