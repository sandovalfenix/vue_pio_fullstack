<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'CounterButtons',
  emits: ['increment'],
})
</script>

<template>
  <div class="counter-buttons">
    <button @click="$emit('increment')">+1 (desde componente)</button>
    <button @click="$emit('increment')">Otro +1</button>
  </div>
</template>

<style scoped>
.counter-buttons {
  display: inline-flex;
  gap: 0.5rem;
}
button {
  background: #3b82f6;
  color: white;
  border: none;
  padding: 0.45rem 0.6rem;
  border-radius: 4px;
  cursor: pointer;
}
button:hover {
  opacity: 0.9;
}
</style>
