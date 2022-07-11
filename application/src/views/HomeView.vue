<template>
    <div class="home">
        <h1>Movie list</h1>
        <movie-list />
    </div>
</template>

<script setup>
import { onMounted, ref } from 'vue';
import MovieList from '@/components/MovieList.vue';
import axios from 'axios';

const url = 'https://api.themoviedb.org/3/collection/10';
const configuration = {
    headers: {
        Authorization: 'Bearer eyJhbGciOiJIUzI1NiJ9.eyJhdWQiOiJiYjVjYzI4NzJhODg0MDEyOTdhMzVjNDU3YzdhMGZiYyIsInN1YiI6IjYyY2MxMGM5ZTgxMzFkMGZiYWRhMTJkZSIsInNjb3BlcyI6WyJhcGlfcmVhZCJdLCJ2ZXJzaW9uIjoxfQ.lJfq32ClHajArPLSrQNGb6sTobPmOWfTL3En3rE1fPI'
    }
}

const movies = ref([]);

onMounted(async () => {
    // TODO: Zapytanie przez Axiosa
    // TODO: Wyciągnij filmy poprzez element 'parts' zwrócony przez zapytanie (`[dane z zapytania].parts`)
})
</script>
