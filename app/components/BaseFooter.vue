<script lang="ts" setup>
import { isClient } from '@vueuse/core'

const displayICP = ref(true)
</script>

<template>
  <div p="4 t-2" class="flex flex-col items-center justify-center" text="sm">
    <CurrentVersion />
  </div>
</template>
