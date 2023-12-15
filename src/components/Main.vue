<script setup>
    import MainSearch from './MainSearch.vue'
    import MainCards from './MainCards.vue'
</script>

<template>
    <div class="wrapper">
        <MainSearch />
        <MainCards />
        <h1>Hello There</h1>
    </div>
</template>

<style scopred lang="postcss">
    .wrapper {
        @apply container mx-auto flex flex-col py-6 gap-6;
    }
</style>