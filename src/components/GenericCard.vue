<script setup lang="ts">
import type { Children } from '@/types/uiConfig'
import MetadataProcessor from './MetadataProcessor.vue'

interface Props {
  title: string
  styles: string
  children: Children
}

const { title, styles, children } = defineProps<Props>()
</script>

<template>
  <div class="mb-14 max-w-xl p-6 bg-white border border-gray-200 rounded-lg shadow" :class="styles">
    <h3 class="mb-4 text-xl font-extrabold leading-none tracking-tight text-gray-900">
      {{ title }}
    </h3>
    <MetadataProcessor v-if="children" :children="children" />
  </div>
</template>
