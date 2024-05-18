<script setup>
import { ref } from "vue";
let tab = ref(1);
import Home from "./Home.vue";
import ProductsToBuy from "./ProductsToBuy.vue";

</script>

<template>
  <div class="tabs w-full">
  <!-- Tabs -->
    <div class="flex justify-center p-5">
      <button :class="{'btn-neutral' : tab === 1 }" class="btn btn-xs sm:btn-sm md:btn-md lg:btn-lg" @click="tab=1">Home</button>
      <button :class="{'btn-neutral' : tab === 2 }" class="btn btn-xs sm:btn-sm md:btn-md lg:btn-lg" @click="tab=2">Prodotti da acquistare</button>
    </div>
    <!-- Contenuto -->
    <div class="contents">
      <div v-if="tab == 1" class="py-10 px-6">
      <Home/>
      </div>
      <div v-if="tab == 2" class="py-10 px-6">
      <ProductsToBuy/>
      </div>
    </div>
  </div>
</template>


