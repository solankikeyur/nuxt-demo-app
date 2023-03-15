<template>
  <div class="block relative h-52 rounded overflow-hidden">
    <img
      :alt="product.title"
      class="object-center w-full h-full block"
      :src="product.image"
    />
  </div>
  <div class="mt-4">
    <h3 class="text-gray-500 text-xs tracking-widest title-font mb-1">
      {{ product.category }}
    </h3>
    <h2 class="text-gray-900 title-font text-lg font-medium">
      {{ product.title }}
    </h2>
    <p class="mt-1">${{ product.price }}</p>
  </div>
</template>
<script setup>
defineProps({
    product: {
      type: Object,
      required: true
    }
})
</script>