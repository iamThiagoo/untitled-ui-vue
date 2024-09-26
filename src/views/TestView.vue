<script setup lang="ts">
import Badge from '@/components/badge/Badge.vue'
import type { IButtonGroup } from '@/components/button-group/@types/button-group'
import ButtonGroup from '@/components/button-group/ButtonGroup.vue'

const buttonsConfig: IButtonGroup[] = [
  {
    label: 'Test',
    id: '1',
    customClass: ''
  },
  {
    label: 'Test 2',
    id: '2',
    customClass: ''
  },
  {
    label: 'Test',
    id: '3',
    customClass: ''
  }
]
</script>

<template>
  <ButtonGroup :buttonsConfig="buttonsConfig" />
  <Badge label="Label" />
</template>
