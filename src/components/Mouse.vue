<script setup lang="ts">
import { useMouse, usePreferredDark, useLocalStorage } from '@vueuse/core'

const { x, y } = useMouse()

const isDark = usePreferredDark()
console.log(isDark.value)

const store = useLocalStorage('my-storage', {
  name: 'Apple',
  color: 'red',
})
console.log(store.value)
</script>

<template>
  <h3>Mouse: {{ x }} x {{ y }}</h3>
</template>

<style scoped></style>
