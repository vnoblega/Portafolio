<script setup>
import { ref, computed } from 'vue'

const alumnos = ref([
  { id: 1, nombre: 'Juan' },
  { id: 2, nombre: 'María' },
  { id: 3, nombre: 'Carlos' }
])

const totalAlumnos = computed(() => alumnos.value.length)
</script>

<template>
  <div class="alumnos">
    <h3>Total de alumnos: {{ totalAlumnos }}</h3>
    <ul>
      <li v-for="alumno in alumnos" :key="alumno.id">
        {{ alumno.nombre }}
      </li>
    </ul>
  </div>
</template>

<style scoped>
.alumnos {
  padding: 1rem;
}

ul {
  list-style: none;
  padding: 0;
}

li {
  margin-bottom: 0.5rem;
}
</style>
