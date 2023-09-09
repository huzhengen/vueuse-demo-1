<script setup lang="ts">
import { ref } from 'vue'
import { useClipboard } from '@vueuse/core'

const source = ref('Copy this text')

const { text, copy, copied, isSupported } = useClipboard({ source })
</script>

<template>
  <div v-if="isSupported">
    <button @click="copy(source)">
      <!-- by default, `copied` will be reset in 1.5s -->
      <span v-if="!copied">{{ source }}</span>
      <span v-else style="color: green">Copied!</span>
    </button>
    <p>
      Current copied: <code>{{ text || 'none' }}</code>
    </p>
  </div>
  <p v-else>Your browser does not support Clipboard API</p>
  <hr />
</template>

<style scoped></style>
