<script setup>
import { ref } from 'vue'
const brand = ref('🚗Lopez Automotive')
</script>


<template>
    <nav class="bg-blue-900">
    <div class="wrapper">
      <div class="brand">
        <span class="brand-title">[{Lopez Automotive }]</span>
      </div>
      <div class="menu">
        <a href="#" class="menu-item">Vehicles</a>
        <a href="#" class="menu-item">Settings</a>
        <a href="#" class="menu-item">Logout</a>
      </div>
    </div>
  </nav>
</template>

<style scoped lang="postcss">
nav {
  @apply flex h-20 bg-slate-800 text-slate-100;
 .wrapper {
  @apply container mx-auto flex w-full items-center justify-between;
  .brand {
        &-title {
          @apply text-2xl font-bold text-teal-800;
        }
      }
      .menu {
        @apply flex gap-2;
        div {
          @apply px-4 py-2;
        }
        &-item {
          @apply rounded-md px-4 py-2 hover:bg-green-500 hover:text-slate-900;
        }
        &-login {
          @apply rounded-md bg-blue-800 px-4 py-2 text-red-100 hover:bg-purple-700;
        }
         &-logout {
          @apply rounded-md bg-blue-700 px-4 py-2 text-blue-200 hover:bg-slate-700;
        }
      }
 }
}
</style>