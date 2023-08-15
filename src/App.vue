<template>
  <div class="layout">
    <RouterView />
  </div>
</template>
<script setup lang="ts">
import { RouterView } from 'vue-router'
</script>

<style lang="scss" scoped>
.layout {
  // max-width: 1440px;
  margin: 0 auto;
  background: #000;
}
</style>
