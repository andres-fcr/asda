<template>
	<HelloWorld v-if="modal" @modal="toggleModal" />
	<button @mouseover="toggleModal" class="p-3 bg-slate-500 text-white">Open modal</button>
</template>

<script setup>
import {ref} from "vue";
import HelloWorld from "./components/HelloWorld.vue";
const modal = ref(false);
const toggleModal = () => {
	modal.value = !modal.value;
};
</script>
<style scoped>
.logo {
	height: 6em;
	padding: 1.5em;
	will-change: filter;
	transition: filter 300ms;
}
.logo:hover {
	filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
	filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
