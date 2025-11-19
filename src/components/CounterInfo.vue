<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'CounterInfo',
  props: {
    count: { type: Number, required: true },
    doubleCount: { type: Number, required: true },
  },
})
</script>

<template>
  <div class="counter-info">
    <p><strong>Valor:</strong> {{ count }}</p>
    <p><strong>El doble:</strong> {{ doubleCount }}</p>
  </div>
</template>

<style scoped>
.counter-info {
  background: #f6f8fa;
  padding: 0.75rem;
  border-radius: 6px;
  margin-bottom: 0.75rem;
}
</style>
