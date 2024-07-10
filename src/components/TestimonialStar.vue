<template>
  <div class="bg-[#F1ECE6] w-[300px] rounded rounded-lg px-10 py-10 w-[408px] h-[276px]">
    <div class="flex">
      <img :src="picture" class="w-24 h-24" />
      <div class="px-2 py-2">
        <p class="text-xl font-semibold">{{ name }}</p>
        <div class="flex flex-row">
          <div v-for="items in star" class="">
            <svg xmlns="http://www.w3.org/2000/svg" width="22px" height="22px" viewBox="0 0 24 24">
              <path
                fill="#FFA500"
                d="m5.825 22l1.625-7.025L2 10.25l7.2-.625L12 3l2.8 6.625l7.2.625l-5.45 4.725L18.175 22L12 18.275z"
              ></path>
            </svg>
          </div>
        </div>
      </div>
    </div>
    <div class="pt-6">
      <p>{{ comment }}</p>
    </div>
  </div>
</template>

<script setup>
defineProps({
  picture: {
    type: String,
    required: true
  },
  name: {
    type: String,
    required: true
  },
  star: {
    type: Number,
    required: true
  },
  comment: {
    type: String,
    required: true
  }
})
</script>
