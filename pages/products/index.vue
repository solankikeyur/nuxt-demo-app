<template>
  <head>
    <title>Nuxt Demo | Products</title>
  </head>
  <div v-if="pending">
    <TheLoader></TheLoader>
  </div>
  <section class="text-gray-600 body-font" v-else>
    <div class="container px-5 py-24 mx-auto">
      <div class="flex flex-wrap -m-4">
        <div
          class="lg:w-1/5 md:w-1/3 p-4 w-full"
          v-for="product in products"
          :key="product.id"
        >
          <NuxtLink :to="`/products/${product.id}`">
            <ProductListCard :product="product" ></ProductListCard>
          </NuxtLink>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
definePageMeta({
  layout: "products",
});
const { pending, data: products } = useLazyFetch(
  "https://fakestoreapi.com/products"
);
</script>
