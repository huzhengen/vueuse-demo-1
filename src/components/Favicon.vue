<script setup lang="ts">
import { useFavicon } from '@vueuse/core'

const icon = useFavicon()

// icon.value = 'https://vueuse.org/favicon-32x32.png' // change current icon
icon.value = 'https://cn.vitejs.dev/logo.svg'
console.log(icon.value)
</script>

<template>
  <div>
    {{ icon }}
  </div>
  <hr />
</template>

<style scoped></style>
