<script setup lang="ts">
interface Props {
  modelValue: number
  title: string
}
withDefaults(defineProps<Props>(), {
  title: "Step"
})

const emit = defineEmits(["update:modelValue"])
const updateValue = (event: Event) => {
  emit("update:modelValue", (event.target as HTMLInputElement).value)
}
</script>
<template>
  <div class="input">
  {{title}}
  <input     
      :value="modelValue"
      @input="updateValue"
  />
  </div>
</template>


<style scoped>
.input {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
