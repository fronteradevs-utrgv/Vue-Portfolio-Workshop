<script setup>
import {onMounted, onUpdated } from 'vue';
import AboutMe from '@/components/about/AboutMe.vue';
import feather from 'feather-icons';
onMounted(() => {
	feather.replace();
});
onUpdated(() => {
	feather.replace();
});
</script>

<template>
<div>
	<!-- About me -->
	<div class="container mx-auto">
		<AboutMe />
	</div>
</div>
</template>

<style scoped></style>
