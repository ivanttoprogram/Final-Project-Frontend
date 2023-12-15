<script setup>
import MainCardSingle from '@/components/MainCardSingle.vue'
</script>

<template>
  <div class="sub-wrapper">
  <MainCardSingle v-for="n in 20" :key="n"/>
  </div>
</template>

<style scoped lang="postcss">
  .wrapper{
  @apply grid grid-cols-1 gap-4 md:grid-cols-2 lg:grid-cols-2 xl:grid-cols-4;
  }
</style>