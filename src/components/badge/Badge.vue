<script setup lang="ts">
const props = defineProps<{
  label: string
  customClasses?: string
}>()
</script>

<template>
  <div
    class="border border-red-400 bg-red-200 rounded-full p-1 px-2 text-sm w-max"
    :class="customClasses"
  >
    {{ props.label }}
  </div>
</template>
