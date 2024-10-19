<script lang="ts" setup>
const rStore = useRecipeStore()

const searchInput = ref<HTMLInputElement>()
onMounted(() => {
  searchInput.value?.focus()
})
</script>

<template>
  <div m="auto b-2" max-w="500px">
    <div relative text-xs>
      <div
        v-if="rStore.keyword" cursor="pointer"
        absolute right-2 inline-flex justify="center" items-center h="full" opacity="70"
        @click="rStore.clearKeyWord()"
      >
        <div i-ri-close-line />
      </div>
    </div>
  </div>
</template>
