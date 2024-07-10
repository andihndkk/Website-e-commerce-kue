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

  <section class="container mx-auto my-52">
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

  <section class="container mx-auto my-52">
    <div class="font-extrabold text-5xl flex justify-center">
      <p>Produk Populer</p>
    </div>
    <div class="flex flex-wrap gap-7 my-8 justify-center">
      <div class="" v-for="items in products">
        <Products :picture="items.picture" :title="items.title" :price="items.price" />
      </div>
    </div>
  </section>

  <section class="bg-[#F1ECE6] flex justify-between items-center my-52">
    <div
      class="px-8 md:px-16 lg:px-48 w-full flex flex-col md:flex-row justify-between items-center"
    >
      <div class="md:w-1/2 mb-8 md:mb-0">
        <h1 class="font-bold text-4xl md:text-5xl lg:text-6xl mb-6">
          Temukan Kue Lezat di Toko Kami
        </h1>
        <p class="text-lg md:text-xl leading-relaxed mb-6">
          Kami tidak hanya menawarkan kue yang lezat, tetapi juga pelayanan terbaik. Tim kami siap
          memberikan informasi yang Anda butuhkan tentang produk kami dan membantu Anda memilih kue
          yang paling sesuai dengan keinginan Anda. Segera mampir ke toko kami dan rasakan
          kenikmatan kue-kue kami. Kami dengan senang hati menantikan kunjungan Anda!
        </p>
        <button
          class="bg-[#680A08] rounded-lg w-[190px] h-[55px] hover:bg-[#734746] transition-colors duration-300 text-white font-semibold text-lg"
        >
          Pesan Sekarang
        </button>
      </div>
      <div class="md:w-1/2 flex justify-end pr-8">
        <img
          src="/public/img/KueEmas.png"
          class="w-full h-auto object-cover rounded-lg shadow-lg max-w-xs md:max-w-sm lg:max-w-md"
        />
      </div>
    </div>
  </section>

  <section class="container mx-auto my-52">
    <div class="font-extrabold text-5xl flex justify-center py-8">
      <h1>Apa kata Mereka</h1>
    </div>
    <div class="flex gap-9 my-8 justify-center">
    <div v-for="items in review">
      <Review :picture="items.picture" :name="items.name" :star="items.star" :comment="items.comment"/>
    </div>
    </div>
  </section>

  <div>
    <Footer />

  </div>
</template>

<script setup>
import Navbar from '../components/navBar.vue'
import Products from '../components/listProduct.vue'
import Review from '../components/TestimonialStar.vue'
import Footer from '@/components/Footer.vue'
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
  }
])

const review = ref([
  {
    picture: '/public/img/avatar.png',
    name: 'Mahluk Bumi',
    star: 5,
    comment: 'Donat dari Cakkeu benar-benar luar biasa! Lembut dan lezat'
  },
  {
    picture: '/public/img/oyentampan.png',
    name: 'Oyen Tampan',
    star: 5,
    comment: 'Cupcake yang indah dan rasanya sempurna, sangat direkomendasikan!'
  },
  {
    picture: '/public/img/hams.png',
    name: 'Hams',
    star: 5,
    comment: 'Macaron dengan rasa yang beragam dan nikmat, favorit saya!'
  },
])
</script>
