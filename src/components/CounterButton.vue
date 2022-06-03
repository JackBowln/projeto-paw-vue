<script setup lang="ts">
import { ref } from 'vue';

interface Props {
  step: number
}
defineProps<Props>()
const count = ref<number>(0)

function increment(step: number = 1) {
  count.value += step
}
</script>
<template>
  <div>
    <button @click="increment(step || 1)">CLICK {{count}}</button>
    <button @click="count = 0">reset</button>
  </div>

  <div v-if="count < 500">
    Número menor que 500
  </div>
  <div v-else-if="count > 500 && count < 1000">
    Número maior que 500 
  </div>
  <div v-else>
    já deu 1000
  </div>
</template>

<style scoped>

</style>
