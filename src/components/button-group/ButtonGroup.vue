<script setup lang="ts">
import type { IButtonGroup } from './@types/button-group'

const props = defineProps<{
  buttonsConfig: IButtonGroup[]
  customClasses?: string
}>()
const emit = defineEmits(['click'])

const onClick = (id: string) => {
  emit('click', id)
}
</script>

<template>
  <div class="flex">
    <button
      v-for="(button, i) in props.buttonsConfig"
      :key="i"
      @click="onClick(button.id)"
      class="border-2 shadow border-[#D0D5DD] m-0 p-3 text-xl font-semibold px-10 hover:opacity-80 focus:outline-none border-2focus:ring-4 transition-200 text-slate-800"
      :class="[
        i == 0 ? 'rounded-l-lg border-r-1' : '',
        i == props.buttonsConfig.length - 1 ? 'rounded-r-lg border-l-1' : '',
        button.customClass
      ]"
    >
      {{ button.label }}
    </button>
  </div>
</template>
