<script setup>
  import { faker } from '@faker-js/faker'

  const Manufacturer = faker.vehicle.manufacturer()
  const Model = faker.vehicle.model()
  const Vehicle = `${Manufacturer} ${Model}`

  const selectCard = () => {
    console.log(`${Vehicle} selected`)
  }
</script>

<template>
  <div class="card" @click="selectCard">
    <div class="card-image">
      <img :src="faker.image.transport(1234, 2345, true)" />
    </div>
    <div class="card-details">
      <p class="card-details-vehicle">{{ Vehicle }}</p>
      <p class="card-details-Type">{{ faker.vehicle.type() }}</p>
      <p class="card-details-Price">{{ faker.commerce.price({ max: 100000 }) }}</p>
      <p class="card-details-Description">"{{ faker.commerce.productDescription() }}"</p>
    </div>
  </div>
</template>

<style scoped lang="postcss">
  .card {
    @apply cursor-pointer overflow-hidden rounded-md bg-slate-200 p-8 shadow-md transition-transform duration-300 hover:scale-110 hover:shadow-2xl hover:shadow-slate-800;
    &-image {
      img {
        @apply mx-auto rounded-full object-contain;
      }
    }
    &-details {
      @apply flex flex-col gap-2  pt-6 text-center;
      &-name {
        @apply text-3xl font-bold  tracking-wider text-slate-800;
      }
      &-job {
        @apply -mt-2 text-xs font-bold text-yellow-500;
      }
      &-email {
        @apply text-sm text-slate-700;
      }
      &-quote {
        @apply pt-4 text-lg italic text-slate-800;
      }
    }
  }
</style>