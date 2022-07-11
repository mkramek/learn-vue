<template>
    <div v-if="movie === undefined">
        <h1 style="color: red">Error: no movie assigned</h1>
    </div>
    <div v-else class="card-container">
        <div class="image-container">
            <img class="image" :src="`https://image.tmdb.org/t/p/w200${movie.poster_path}`" :alt="movie.title" />
        </div>
        <div class="info-container">
            <h3 class="info-title">{{ movie.title }}</h3>
            <p class="info-tmdb-id"><b>TMDB ID:</b> {{ movie.id }}</p>
            <p class="info-release-date"><b>Release date:</b> {{ movie.release_date }}</p>
            <p class="info-overview"><b>Overview:</b> <i>{{ movie.overview }}</i></p>
        </div>
    </div>
</template>

<script setup>
// TODO: Stworzyć właściwość "movie"
</script>

<style scoped lang="scss">
.card-container {
    display: flex;
    flex-flow: row nowrap;
    max-width: 40rem;
    max-height: 25rem;
    margin: 15px auto;
    box-shadow: 5px 5px 15px #999;
    border-radius: 15px;
}

.image-container {
    display: flex;
    justify-content: center;
    align-items: center;
}

.image {
    border-radius: 15px;
    padding: 5px;
}

.info-tmdb-id,
.info-release-date,
.info-overview {
    text-align: justify;
    padding: 0 10px;
}
</style>