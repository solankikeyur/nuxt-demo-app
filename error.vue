<template>
	<section class="flex items-center h-full p-16">
		<div class="container flex flex-col items-center justify-center px-5 mx-auto my-8">
			<div class="max-w-md text-center">
				<h2 class="mb-8 font-extrabold text-9xl dark:text-gray-600">
					<span class="sr-only">Error</span>{{ error.statusCode }}
				</h2>
				<p class="text-2xl font-semibold md:text-3xl">{{error.message}}</p>
				<p class="mt-4 mb-8 dark:text-gray-400"></p>
				<button class="px-8 py-3 font-semibold rounded dark:bg-green-500 dark:text-gray-900" @click="handleError">Back to homepage</button>
			</div>
		</div>
	</section>
</template>
<script setup>
defineProps({
    error: Object
})
const handleError = () => clearError({ redirect: '/' })
</script>