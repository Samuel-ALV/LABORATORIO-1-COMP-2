<script setup>
import {ref} from 'vue';
import mascota from './componentes/mascota.vue';
import listadeactividades from './componentes/listadeactividades.vue';

const actividades = ref([]);

function agregarActividad(texto){
  actividades.value.push({texto, completada:false});
}

function completarActividad(index){
  actividades.value[index].completada = !actividades.value[index].completada;
}

function eliminarActividad(index){
  actividades.value.splice(index,1);
}
</script>

<template>
  <div class="app-container">
    <div class="card">
      <h1>Agenda de Cuidados de Mascotas (VETERINARIA FFM)</h1>
      <mascota @agregar="agregarActividad"/>
      <listadeactividades :actividades="actividades" 
                          @completar="completarActividad" 
                          @eliminar="eliminarActividad"/>
    </div>
  </div>
</template>

<style>
body {
  font-family: Arial, sans-serif;
  background-color: #f9f9f9;
  margin: 20px;
}

app, body, .app-container {
  min-height: 100vh;
}

.app-container {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 20px;
  box-sizing: border-box;
}

.card {
  width: min(100%, 560px);
  background: white;
  border-radius: 10px;
  padding: 24px;
  box-shadow: 0 8px 30px rgba(0,0,0,0.08);
}

h1 {
  color: #2c3e50;
  text-align: center;
}

input {
  padding: 5px;
  margin-right: 10px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

button {
  padding: 5px 10px;
  background-color: #3498db;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

button:hover {
  background-color: #2980b9;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  margin: 5px 0;
}

.completada {
  text-decoration: line-through;
  color: gray;
}
</style>