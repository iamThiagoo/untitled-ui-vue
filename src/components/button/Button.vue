<script setup lang="ts">
const { label, customClasses } = defineProps<{
  label: string
  customClasses?: string
}>()
const emit = defineEmits(['click'])

const onClick = (event: Event) => {
  emit('click', event)
}
</script>

<template>
  <button
    @click="onClick"
    class="text-white p-3.5 text-xl rounded-xl font-semibold px-10 hover:opacity-80 focus:outline-none border-2 border-white focus:ring-4 focus:ring-red-500 transition-200"
    :class="customClasses"
  >
    {{ label }}
  </button>
</template>
