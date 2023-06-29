<script setup>
const product = ref('');
const router = useRouter();

const searchHandler = () => {
  router.push(`/category/${product.value}/product`);
};
</script>

<template>
  <!-- HomeSearchBar -->
  <div
    class="font-serif w-100 text-2xl rounded-full bg-white flex justify-between overflow-hidden drop-shadow-2xl mx-auto"
  >
    <input
      type="text"
      class="py-3 px-5 w-full text-2xl rounded-full focus:outline-none"
      placeholder="你要找甚麼..."
      v-model="product"
    />
    <button @click="searchHandler" class="bg-sky-500 px-5 text-white">
      Search
    </button>
  </div>
  <!-- HomeSearchBar -->
</template>
