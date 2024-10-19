<script lang="ts" setup>
import type { BottomMenuItem } from '@yunlefun/vue'

const items: BottomMenuItem[] = [
  {
    icon: 'i-ri-bowl-line',
    activeIcon: 'i-ri-bowl-fill',
    title: '干饭',
    to: '/',
  },
  {
    icon: 'i-ri-compass-2-line',
    activeIcon: 'i-ri-compass-2-fill',
    title: '吃什么',
    to: '/random',
  },
]

const route = useRoute()
const router = useRouter()

function onClick(item: BottomMenuItem) {
  // router.push(item.to || '/')
  router.replace(item.to || '/')
}
</script>

<template>
  <YlfBottomMenu shadow-2xl pb="$cook-bottom-menu-padding-bottom">
    <YlfBottomMenuItem
      v-for="item in items"
      :key="item.to"
      :item="item"
      :active="route.path === item.to"
      class="pt-3"
      @click="onClick"
    />
  </YlfBottomMenu>
</template>
