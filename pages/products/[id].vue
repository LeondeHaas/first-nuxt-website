<template>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6 p-6">
      <div class="border p-4 rounded-lg shadow-md bg-white">
        <div class="w-full h-64 mb-4 overflow-hidden flex justify-center">
          <img :src="product.image" alt="Product Image" class="object-contain w-full h-full" />
        </div>
  
        <p class="text-xl font-semibold mb-2">Product details for {{ id }}</p>
        <p class="mb-4">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
  
        <div class="grid grid-cols-1 gap-4">
          <p class="text-lg font-bold">Title: {{ product.title }}</p>
          <p class="text-lg font-semibold text-green-600">Price: ${{ product.price }}</p>
          <p class="text-sm text-gray-500">Product ID: {{ product.id }}</p>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
    const { id } = useRoute().params
  
    const uri = 'https://fakestoreapi.com/products/' + id
    const { data: product } = await useFetch(uri)
  </script>
  