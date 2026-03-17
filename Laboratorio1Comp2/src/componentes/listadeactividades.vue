<script setup>
const props = defineProps({
  actividades: Array
});

const emitir = defineEmits(['completar','eliminar']);
</script>

<template>
  <ul>
    <li v-for="(actividad,index) in actividades" :key="index">
      <span :class="{completada: actividad.completada}">
        {{ actividad.texto }}
      </span>
      <button @click="emitir('completar',index)">SI</button>
      <button @click="emitir('eliminar',index)">NO</button>
    </li>
  </ul>
</template>

<style scoped>
.completada { text-decoration: line-through; color: gray; }

button {
  background-color: rgb(151, 166, 170);
  color: white;
}
</style>