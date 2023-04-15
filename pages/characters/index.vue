<script setup>
const characters = await queryContent('/characters').find()
</script>

<template>
    <div>
        <h2>Characters</h2>
        <div class="characters">
            <LazyCharacter v-for="{title, description, _path} in characters" :title="title" :description="description" :path="_path" :key="title" />
        </div>
    </div>
</template>