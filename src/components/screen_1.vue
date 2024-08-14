
<script setup>
</script>

<template>
    <ul class="anime-grid-box">
        <li v-for="n in 20" class="anime-item">
            <a href="#url"><img src="" alt="anime-cover"></a>
            <span class="anime-data"> titulo do anime: 8.1 | <i class="anime-state">assistindo</i></span>
        </li>
    </ul>
</template>

<style scoped>
    .anime-grid-box {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
        width: 100%;
        height: 90vh;
        overflow: auto;
        border: 1px solid red;
        list-style: none;
    }
        .anime-item {
            cursor: pointer;
            display: block;
            width: 160px;
            height: 240px;
            border: 1px solid #000;
            margin: 2%;
        }
</style>