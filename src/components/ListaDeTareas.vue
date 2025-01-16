

<template>
  <div>
    <h2>Lista de tareas</h2>
    <input type="text" v-model="nuevaTarea" @keyup.enter="addTarea">
    <ul>
      <li v-for="(tarea,index) in tareas" :key="index">
        {{tarea}}
      </li>
    </ul>
  </div>
</template>

<script setup>
  import {ref} from 'vue';
  const tareas = ref([]);//Array de tareas reactivo
  const nuevaTarea = ref('');//

  //Funcion para agregar nuevas tareas al array
  const addTarea = () => {
    tareas.value.push(nuevaTarea.value);
    nuevaTarea.value = '';
  }

</script>

<style scoped>

</style>
