<script setup lang="ts">
definePageMeta({
  layout: "products",
});

const { data: products } = await useFetch("https://fakestoreapi.com/products");
</script>

<template>
  <div>
    <Head>
      <Title>Nuxt-Init | Products</Title>
    </Head>
    <div class="grid grid-cols-4 gap-5">
      <div v-for="product in products">
        <ProductCard :product="product" />
      </div>
    </div>
  </div>
</template>
