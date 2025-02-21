<template>
    <div>
      <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-5 p-6">
        <div v-for="p in products" :key="p.id" class="border p-4 rounded-lg shadow-md bg-white">
          <NuxtLink :to="`/products/${p.id}`" class="block text-center mb-2">
            <img :src="p.image" alt="Product Image" class="object-contain w-full h-40 mb-2" />
            <p class="font-semibold text-center">{{ p.title }}</p>
          </NuxtLink>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
    const { data: products } = await useFetch('https://fakestoreapi.com/products/')
  </script>
  