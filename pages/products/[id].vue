<template>
    <head>
        <title>Next Demo | {{ product.title }}</title>
        <meta name="description" :content="product.description" >
    </head>
  <section class="text-gray-600 body-font overflow-hidden">
    <ProductDetail :product="product" ></ProductDetail>
  </section>
</template>

<script setup>
const { id } = useRoute().params;
const { data: product } = await useFetch(
  `https://fakestoreapi.com/products/${id}`
);

if(!product.value) {
    throw createError({statusCode: 404, statusMessage: 'Product not found.', fatal: true})
}
</script>
