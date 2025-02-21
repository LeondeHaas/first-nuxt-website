<template>
  <div class="flex h-screen">
    <!-- Zijbalk -->
    <aside class="bg-gray-800 text-white w-90 p-7 flex flex-col h-full">
      <div class="text-4xl font-bold mb-6">Leon de Haas</div>
      <ul class="space-y-6 flex-grow">
        <li class="flex items-center space-x-3">
          <NuxtLink 
            to="/" 
            class="w-full flex justify-start items-center py-2.5 bg-transparent hover:bg-gray-700 text-white font-bold text-2xl rounded-lg transition-all duration-300">
            <i class="fa-solid fa-house text-xl mr-3"></i> Home
          </NuxtLink>
        </li>
        <li class="flex items-center space-x-3">
          <NuxtLink 
            to="/about" 
            class="w-full flex justify-start items-center py-2.5 bg-transparent hover:bg-gray-700 text-white font-bold text-2xl rounded-lg transition-all duration-300">
            <i class="fa-solid fa-address-card text-xl mr-3"></i> About
          </NuxtLink>
        </li>
        <li class="flex items-center space-x-3">
          <NuxtLink 
            to="/contact" 
            class="w-full flex justify-start items-center py-2.5 bg-transparent hover:bg-gray-700 text-white font-bold text-2xl rounded-lg transition-all duration-300">
            <i class="fa-solid fa-comment-arrow-up-right text-xl mr-3"></i> Contact
          </NuxtLink>
        </li>
        <li class="flex items-center space-x-3">
          <NuxtLink 
            to="/products" 
            class="w-full flex justify-start items-center py-2.5 bg-transparent hover:bg-gray-700 text-white font-bold text-2xl rounded-lg transition-all duration-300">
            <i class="fa-solid fa-comment-arrow-up-right text-xl mr-3"></i> Products
          </NuxtLink>
        </li>
      </ul>

      <primaryButton />
    </aside>

    <!-- De daadwerkelijke pagina's worden hier geladen -->
    <div class="flex-1 p-7 overflow-auto">
      <NuxtPage />
    </div>
  </div>
</template>

<script>
import primaryButton from '~/components/primaryButton.vue';

export default {
  components: {
    primaryButton,
  },
};
</script>
