<template>
  <div class="bg-[#F1ECE6] flex flex-col w-[300px] rounded rounded-lg">
    <img :src="picture" />
    <div class="font-semibold flex justify-center py-4">
      <div class="flex flex-col">
        <p>{{ title }}</p>
      </div>
    </div>
    <div class="font-semibold flex justify-center pb-4">
      <p>{{ price }}</p>
    </div>
    <div class="flex justify-center pb-5">
      <button class="bg-[#680A08] rounded-lg w-[190px] h-[55px] hover:bg-[#734746]">
        <div class="text-white">Pesan Sekarang</div>
      </button>
    </div>
  </div>
</template>

<script setup>
defineProps({
  picture: {
    type: String,
    required: true
  },
  title: {
    type: String,
    required: true
  },
  price: {
    type: String,
    required: true
  }
})
</script>
