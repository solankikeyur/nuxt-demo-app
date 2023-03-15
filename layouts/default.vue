<template>
  <header class="text-gray-600 body-font">
    <div
      class="container mx-auto flex flex-wrap p-5 flex-col md:flex-row items-center"
    >
      <NuxtLink
        class="flex title-font font-medium items-center text-gray-900 mb-4 md:mb-0"
        to="/"
      >
        <span class="ml-3 text-xl">Nuxt Demo</span>
      </NuxtLink>
      <nav
        class="md:ml-auto flex flex-wrap items-center text-base justify-center"
      >
        <NuxtLink to="/" class="mr-5 hover:text-gray-900">Home</NuxtLink>
        <NuxtLink to="/products" class="mr-5 hover:text-gray-900">Products</NuxtLink>
        <NuxtLink to="/about" class="mr-5 hover:text-gray-900">About</NuxtLink>
      </nav>
    </div>
  </header>
  <slot></slot>
</template>
<style scoped>
nav .router-link-exact-active {
  color: #48bb78;
}
</style>
