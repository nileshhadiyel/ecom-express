<template>
  <MainLayout>
    <div id="IndexPage" calss="mt-4 max-w-[1200px] mx-auto px-2">
      <div class="grid xl:grid-cols-6 lg:grid-cols-5 md:grid-cols-4 md:grid-cols-3 grid-cols-2 gap-4">
        <div v-if="products" v-for="product in products" :key="product">  
          <ProductComponent :product="product" />
        </div>
      </div>
    </div>
  </MainLayout>
</template>
<script setup>
import MainLayout from "../layouts/MainLayout.vue";

const products = [
  {
    id: 1,
    title: "Title 1",
    description: "This is a description",
    url: "https://picsum.photos/id/88/800/800",
    price: 9999,
  },
  {
    id: 2,
    title: "Title 1",
    description: "This is a description",
    url: "https://picsum.photos/id/28/800/800",
    price: 9999,
  },
  {
    id: 3,
    title: "Title 1",
    description: "This is a description",
    url: "https://picsum.photos/id/1/800/800",
    price: 9999,
  },
  {
    id: 4,
    title: "Title 1",
    description: "This is a description",
    url: "https://picsum.photos/id/10/800/800",
    price: 9999,
  },
  {
    id: 4,
    title: "Title 1",
    description: "This is a description",
    url: "https://picsum.photos/id/12/800/800",
    price: 9999,
  },
  {
    id: 5,
    title: "Title 1",
    description: "This is a description",
    url: "https://picsum.photos/id/22/800/800",
    price: 9999,
  },
  {
    id: 1,
    title: "Title 1",
    description: "This is a description",
    url: "https://picsum.photos/id/88/800/800",
    price: 9999,
  },
  {
    id: 2,
    title: "Title 1",
    description: "This is a description",
    url: "https://picsum.photos/id/28/800/800",
    price: 9999,
  },
  {
    id: 3,
    title: "Title 1",
    description: "This is a description",
    url: "https://picsum.photos/id/1/800/800",
    price: 9999,
  },
  {
    id: 4,
    title: "Title 1",
    description: "This is a description",
    url: "https://picsum.photos/id/10/800/800",
    price: 9999,
  },
  {
    id: 4,
    title: "Title 1",
    description: "This is a description",
    url: "https://picsum.photos/id/12/800/800",
    price: 9999,
  },
  {
    id: 5,
    title: "Title 1",
    description: "This is a description",
    url: "https://picsum.photos/id/22/800/800",
    price: 9999,
  },
];
</script>
