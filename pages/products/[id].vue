<template>
  <div class="container mx-auto">
    <ProductDetails :product="product"/>
  </div>
</template>

<script setup>
const { id } = useRoute().params;
const uri = "https://fakestoreapi.com/products/" + id;

// fetch
const { data: product } = await useFetch(uri, { key: id });
definePageMeta({
  layout: "products",
});
</script>

<style  scoped>
</style>