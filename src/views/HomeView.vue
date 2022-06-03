<script setup lang="ts">
import { ref } from "vue";
import CounterButton from "../components/CounterButton.vue";
import CounterInput from "../components/CounterInput.vue";


const stepText = ref<number>();
</script>

<template>
  <main >
    <h1>Contador</h1>
    <CounterButton
      :step="parseInt(stepText)"
    />
    <CounterInput 
    v-model="stepText"
    />
    {{stepText}}
  </main>
</template>
