<script lang="ts" setup>
const rStore = useRecipeStore()
</script>

<template>
  <div>
    <div text-4xl>
      <button
        class="cursor-pointer transition active:text-green-800 hover:(text-green-600)"
        title="重置"
        @click="rStore.reset"
      >
        <div v-if="rStore.selectedStuff.length" i-mdi-pot-steam-outline />
        <div v-else i-mdi-pot-mix-outline />
      </button>
    </div>
    <p style="font-size: 50px; margin-bottom: 16px; border: 2px solid #000; padding: 10px;">
      兄dei,今晚吃啥！
    </p>

    <ChooseFood />
    <SimpleCopyright />
  </div>
</template>
