
<script setup>
	import {ref, defineAsyncComponent} from "vue"

	const current_screen = ref(defineAsyncComponent(() => import('./components/screen_1.vue')));

	const goto_screen = (number) => {
		switch(number) {
			case 1: current_screen.value = defineAsyncComponent(() => import('./components/screen_1.vue')); break;
			case 2: current_screen.value = defineAsyncComponent(() => import('./components/screen_2.vue'));	break;
			case 3: current_screen.value = defineAsyncComponent(() => import('./components/screen_3.vue'));	break;
			case 4: current_screen.value = defineAsyncComponent(() => import('./components/screen_4.vue'));	break;
		}
	}
</script>

<template>
    <header>
    	<nav class="head-menu-box">
			<button @click="goto_screen(1)">Novos</button>
			<button @click="goto_screen(2)">Assistidos</button>
			<button @click="goto_screen(3)">Dublados</button>
			<button @click="goto_screen(4)">Favoritos</button>
			<input class="search-box" type="url" placeholder="Procurar por titulo"/>
			<img src="" alt="sun icon for change theme color" id="change-theme-ic"/>
			<img src="" alt="filter icon" id="change-gener-ic"/>
		</nav>
    </header>
	
    <main class="t-main">
		<component :is="current_screen"/>
	</main>
</template>

<style scoped>
</style>
