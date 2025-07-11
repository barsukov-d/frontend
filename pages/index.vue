<script setup lang="ts">
// 1. Get the `getItems` function from the `useDirectusItems` composable.
const { getItems } = useDirectusItems()

// 2. Use `useAsyncData` to fetch the data.
//    - 'section_hero_data' is a unique key for this fetch.
//    - The second argument is the function that fetches your data.
const {
	data: heroSection,
	pending,
	error,
} = useAsyncData('section_hero_data', () =>
	getItems({
		collection: 'section_hero',
		// You can add any additional Directus query parameters here
		// params: {
		//   fields: ['title', 'subtitle', 'image'],
		// },
	})
)
</script>

<template>
	<div>
		<!-- Optional: Show a loading message while data is being fetched -->
		<div v-if="pending">Loading hero section...</div>

		<!-- Optional: Show an error message if the fetch fails -->
		<div v-else-if="error">Could not load hero section. Error: {{ error.message }}</div>

		<!-- Display your data when it's available -->
		<div v-else-if="heroSection">
			<h1 class="text-3xl font-bold underline">Hero Section Content</h1>
			<!-- The output of `getItems` is typically an array of items. -->
			<!-- You may need to loop through it or access the first element. -->
			<pre>{{ heroSection }}</pre>
		</div>

		<h1 class="text-3xl font-bold underline">Hello World</h1>
	</div>
</template>
