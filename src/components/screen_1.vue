
<script setup>
</script>

<template>
    <ul class="anime-grid-box">
        <li v-for="n in 20" class="anime-item">
            <a href="#url"><img src="./resources/default_cover.jpg" alt="anime-cover" class="item-cover"></a>
            <span class="item-data"> titulo do anime: 8.1 | <i class="item-state">assistindo</i></span>
        </li>
    </ul>
</template>

<style scoped>
    .anime-grid-box {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
        gap: 10px;
        width: 100%;
        height: 90vh;
        overflow: auto;
        list-style: none;
        /* padding-top: 2%; */
    }
        .anime-item {
            cursor: pointer;
            display: block;
            width: 190px;
            height: 270px;
            box-shadow: 1px 1px 3px 2px #000;
            /* margin: 1%; */
        }
            .item-cover {
                display: block;
                width: 100%;
                height: 240px;
            }
            .item-data {
                display: block;
                width: 100%;
                background-color: #000;
                color: var(--fgcolor);
            }
</style>