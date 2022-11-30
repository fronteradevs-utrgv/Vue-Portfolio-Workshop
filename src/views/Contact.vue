<script setup>
import { onMounted, onUpdated, ref } from 'vue';

import feather from 'feather-icons';
import ContactForm from '@/components/contact/ContactForm.vue';
import ContactDetails from '@/components/contact/ContactDetails.vue';
onMounted(() => {
	feather.replace();
});
onUpdated(() => {
	feather.replace();
});
let contacts = ref([
	{
		id: 1,
		name: 'Your Address, Your City, Your Country',
		icon: 'map-pin',
	},
	{
		id: 2,
		name: 'email@domain.com',
		icon: 'mail',
	},
	{
		id: 3,
		name: '555 8888 888',
		icon: 'phone',
	},
]);

</script>

<template>
	<div class="container mx-auto flex flex-col-reverse md:flex-row py-5 md:py-10 md:mt-10">
		<!-- Contact form -->
		<ContactForm />

		<!-- Contact details -->
		<ContactDetails :contacts="contacts" />
	</div>
</template>
