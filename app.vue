<script setup lang="ts">
import Menu from '@/components/Menu.vue'

console.log('v2')
</script>

<template>
  <div class="layout">
    <div class="page-content">
      <NuxtPage />
      <Menu />
    </div>
  </div>
</template>

<style lang="scss">
.layout {
  width: 100%;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background-image: url('/background.jpg');
  background-size: 100% 100%;

  .page-content {
    position: relative;
    min-width: 800px;
    min-height: 500px;
    padding: 20px 20px 80px;
    background: rgba(22, 22, 22, .7);
    border-radius: 8px;

    .menu {
      position: absolute;
      bottom: 20px;
      left: 50%;
      transform: translateX(-50%);
    }
  }
}
</style>