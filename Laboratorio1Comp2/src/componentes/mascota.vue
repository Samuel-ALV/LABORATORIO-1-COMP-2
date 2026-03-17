<script setup>
import {ref} from 'vue';

const nuevaActividad = ref('');
const error = ref('');

const emitir = defineEmits(['agregar']);

function agregar(){
  if(nuevaActividad.value.trim() === ''){
    error.value = 'La actividad no puede estar vacía';
    return;
  }
  emitir('agregar', nuevaActividad.value);
  nuevaActividad.value = '';
  error.value = '';
}
</script>

<template>
  <div>
    <input v-model="nuevaActividad" type="text" placeholder="Ej: Vacunar al perro">
    <button @click="agregar">Agregar</button>
    <p v-if="error" style="color:red">{{ error }}</p>
  </div>
</template>

<style scoped>
button {
  background-color: green;
  color: white;
}
</style>