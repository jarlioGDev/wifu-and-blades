<script setup lang="ts">
defineProps<{
    title?: string
    description?: string,
    path: string
}>()
</script>

<template>
    <div class="card">
        <h2 class="title"><NuxtLink :href="path">{{ title }}</NuxtLink></h2>
        <div class="description">{{ description }}</div>
    </div>
</template>