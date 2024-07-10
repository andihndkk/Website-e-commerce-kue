<template>
  <div>
    <Navbar />
  </div>

  <section class="bg-[#F1ECE6] container mx-auto">
    <div
      class="gap-16 items-center py-8 px-4 mx-auto max-w-screen-xl lg:grid lg:grid-cols-2 lg:py-16 lg:px-6"
    >
      <div class="text-black">
        <h2 class="mb-4 text-4xl font-extrabold text-black lg:text-6xl">
          Selamat Datang di CAKKEU
        </h2>
        <p class="mb-4 py-4">
          "Nikmati aneka kue kami yang dibuat dengan cinta dan bahan berkualitas tinggi. Dari
          macaron berwarna-warni hingga donat lembut dan cupcake yang cantik, setiap gigitan adalah
          momen istimewa."
        </p>
        <button class="bg-[#680A08] rounded-lg w-[190px] h-[55px] hover:bg-[#734746]">
          <div class="text-white">Pesan Sekarang</div>
        </button>
      </div>
      <div class="flex justify-end">
        <div class="">
          <img class="h-80 w-96" src="/public/img/Kueh.png" />
        </div>
      </div>
    </div>
  </section>
  <section class="container mx-auto my-8">
    <div></div>
    <div class="font-extrabold text-5xl flex justify-between">
      <p>Kategori Produk</p>
      <button class="bg-[#680A08] rounded-lg w-[190px] h-[55px] hover:bg-[#734746]">
        <div class="text-white text-sm">Selengkapnya</div>
      </button>
    </div>
    <div class="flex justify-center py-8">
      <div>
        <img src="/public/img/Cupcake.png" class="p-2.5" />
        <p class="flex justify-center">Cupcake</p>
      </div>
      <div>
        <img src="/public/img/Cupcake.png" class="p-2.5" />
        <p class="flex justify-center">Donat</p>
      </div>
      <div>
        <img src="/public/img/Cupcake.png" class="p-2.5" />
        <p class="flex justify-center">Macaron</p>
      </div>
    </div>
  </section>

  <section class="bg-[#F1ECE6] container mx-auto flex">
    <div>
      <img src="/public/img/KueEmas.png" />
    </div>
    <div class="p-8">
      <p class="font-bold text-3xl">Mengapa Memilih Cakkeu?</p>
      <p class="w-80">
        Cakkeu adalah toko kue yang berdedikasi untuk menyediakan kue-kue berkualitas tinggi yang
        tidak hanya lezat tapi juga indah dipandang. Kami menggunakan bahan-bahan terbaik untuk
        memastikan setiap gigitan adalah pengalaman yang tak terlupakan.
      </p>
      <div>
        <button class="bg-[#680A08] rounded-lg w-[190px] h-[55px] hover:bg-[#734746]">
          <div class="text-white">Pesan Sekarang</div>
        </button>
      </div>
    </div>
  </section>

  <section class="container mx-auto my-12">
    <div class="font-extrabold text-5xl flex justify-center">
      <p>Produk Populer</p>
    </div>
    <div class="flex flex-wrap gap-7 my-8 justify-center" >
      <div class="" v-for="items in products">
        <Products :picture="items.picture" :title="items.title" :price="items.price" />
      </div>
    </div>
  </section>
</template>

<script setup>
import Navbar from '../components/navBar.vue'
import Products from '../components/listProduct.vue'
import { ref } from 'vue'

const products = ref([
  {
    picture: '/public/img/cupcakeEmas.png',
    title: 'Cake Milkshake',
    price: 'Rp25.000'
  },
  {
    picture: '/public/img/redvelvet.png',
    title: 'Red velvet Choco',
    price: 'Rp15.000'
  },
  {
    picture: '/public/img/milkyoreo.png',
    title: 'Milky Oreo',
    price: 'Rp20.000'
  },
  {
    picture: '/public/img/chocomatcha.png',
    title: 'Choco Matcha',
    price: 'Rp.20.000'
  },
  {
    picture: '/public/img/chocomagma.png',
    title: 'Choco Magma Caramel ',
    price: 'Rp.20.000'
  },
  {
    picture: '/public/img/cherry.png',
    title: 'Cherry  Milkshake ',
    price: 'Rp.25.000'
  },
  {
    picture: '/public/img/chocomarcaroon.png',
    title: 'Choco Macaroon',
    price: 'Rp.15.000'
  },
  {
    picture: '/public/img/vanilamilshake.png',
    title: 'Vanila milshake',
    price: 'Rp.25.000'
  },

])
</script>
