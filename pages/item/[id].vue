<template>
  <MainLayout>
    <div id="ItemPage" class="mt-4 max-w-[1200px] mx-auto px-2">
      <div class="md:flex gap-4 justify-between mx-auto w-full">
        <div class="md:w-[40%]">
          <div
          v-if="currentImage"
            class="rounded-lg object-fit"
            :src="currentImage"
          ></div>
          <div v-if="images[0] !== ''" class="flex items-center justify-center mt-2">
            <div v-for="image in images">
              <img
                @mouseover="currentImage = image"
                @click="currentImage = image"
                width="70"
                class="rounded-md object-fit border-[3px] cursor-pointer"
                :class="currentImage === image ? 'border-[#FF5353]' : ''"
                :src="image"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </MainLayout>
</template>

<script setup>
import MainLayout from "~/layouts/MainLayout.vue";

let currentImage = ref(null);

onMounted(() => {
  watchEffect(() => {
    currentImage.value = "https://picsum.photos/id/99/800/800";
    images.value[0] = "https://picsum.photos/id/99/800/800";
  });
});

const images = ref([
  "",
  "https://picsum.photos/id/221/800/800",
  "https://picsum.photos/id/233/800/800",
  "https://picsum.photos/id/244/800/800",
  "https://picsum.photos/id/67/800/800",
  "https://picsum.photos/id/22/800/800",
]);
</script>
