<script setup>
import { useRouter } from 'vue-router';
import ProjectsGrid from '../components/projects/ProjectsGrid.vue';

const router = useRouter();

// This is just to give this component a name for vue-router
router.push({
	name: 'Projects'
});
</script>

<template>
	<div class="container mx-auto">
		<ProjectsGrid />
	</div>
</template>

<style scoped></style>
