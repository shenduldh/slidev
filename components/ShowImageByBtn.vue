<script setup lang="ts">
import { ref } from 'vue';
defineProps<{ imgSrc: string; btnName: string }>();
const isShow = ref(false);
</script>

<template>
	<div>
		<button class="btn" @click="isShow = true">{{ btnName }}</button>
		<div @click="isShow = false" v-show="isShow" class="mask"></div>
		<img v-show="isShow" :src="imgSrc" />
	</div>
</template>

<style scoped>
img {
	z-index: 2;
	position: fixed;
	top: 50%;
	left: 50%;
	transform: translate(-50%, -50%);
}
.mask {
	z-index: 1;
	position: fixed;
	top: 0;
	left: 0;
	width: 100vw;
	height: 100vh;
	background-color: rgba(0, 0, 0, 0.397);
}
.btn {
    padding: 5px;
    box-shadow: 0 0 6px 2px #eee;
    border-radius: 6px;
	outline: none;
}
.btn:hover {
	box-shadow: 0 0 6px 3px #eee;
	background-color: rgba(238, 238, 238, 0.5);
}
.btn:active {
	background-color: rgba(238, 238, 238, 1);
}
</style>
