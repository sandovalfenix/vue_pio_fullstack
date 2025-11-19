<script setup lang="ts">
import { useCounterStore } from './stores/counter'
import CounterInfo from './components/CounterInfo.vue'
import CounterButtons from './components/CounterButtons.vue'

const counter = useCounterStore()

function increment() {
  counter.increment()
}
</script>

<template>
  <div id="app">
    <h1>Ejemplo: Pinia + Componentes en Vue 3</h1>
    <p>
      Este ejemplo usa el store desde <code>src/stores/counter.ts</code> y muestra cómo usarlo en
      componentes.
    </p>

    <CounterInfo :count="counter.count" :double-count="counter.doubleCount" />

    <div class="controls">
      <button @click="increment">Incrementar desde App</button>
      <CounterButtons @increment="increment" />
    </div>

    <hr />
    <p>
      Lectura directa desde el store: <code>{{ counter.count }}</code>
    </p>
  </div>
</template>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  padding: 1.25rem;
}
.counter-info {
  background: #f6f8fa;
  padding: 0.75rem;
  border-radius: 6px;
  margin-bottom: 0.75rem;
}
.controls {
  display: flex;
  gap: 0.5rem;
  align-items: center;
  margin-top: 0.5rem;
}
button {
  background: #3b82f6;
  color: white;
  border: none;
  padding: 0.5rem 0.75rem;
  border-radius: 4px;
  cursor: pointer;
}
button:hover {
  opacity: 0.9;
}
</style>
