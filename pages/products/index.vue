<template>
  <div class="container mx-auto">
    <h2 class="font-bold text-xl text-center py-5">Product page</h2>
    <div class="grid grid-cols-4 gap-5">
      <div v-for="p in products" :key="p.id">
        <ProductCard :product="p" />
      </div>
    </div>
  </div>
</template>

<script setup>
definePageMeta({
  layout: "products",
});

// fetch the products
const { data: products } = await useFetch("https://fakestoreapi.com/products");
</script>

<style scoped>
</style>