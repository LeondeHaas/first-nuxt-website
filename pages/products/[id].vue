<template>
    <div>
        <p>Product details for {{ id }} </p>
        <p>lorem ipsum</p>

        <p>{{ product.title }}</p>
        <p>{{ product.price }}</p>
        <p>{{ product.id }}</p>
    </div>
</template>

<script setup>
    const { id } = useRoute().params

    const uri = 'https://fakestoreapi.com/products/' + id

    // fetch

    const { data: product } = await useFetch(uri)
</script>
