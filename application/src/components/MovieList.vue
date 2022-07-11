<template>
    <template v-if="movies === undefined">
        <h2 style="color: red">Error: no movies defined</h2>
    </template>
    <template v-else>
        <movie-card />
    </template>
</template>

<script setup>
import MovieCard from './MovieCard.vue';

// TODO: Stworzyć właściwość "movies"
</script>