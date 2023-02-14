<template>
	<div ref="box">
		<div class="bg-white rounded text-black">
			texto de prueba {{ numero }}
			<input type="number" name="asd" id="asd" v-model="numero" />
			<button @mouseover="toggle">close</button>
		</div>
	</div>
</template>
<script setup>
import {ref} from "vue";
const numero = ref(0);
const emit = defineEmits(["modal"]);

const toggle = () => {
	emit("modal");
};
</script>

<style scoped>
.read-the-docs {
	color: #888;
}
</style>
