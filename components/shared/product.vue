<script setup lang="ts">
import {products} from '~/constants'
const setItem = ()=>{
  localStorage.setItem("products", "s")
}
</script>

<template>
    <div class="sm:w-[210px] w-full flex gap-4 flex-col items-center justify-between mx-4 shadow-md rounded-lg p-3" v-for="(item, index) in products" :key="index">
        <img :src="item.img" :alt="item.name">
        <h4>{{ item.name }}</h4>
        <span>${{ item.price }}</span>
        <UButton color="orange" size="sm" @click="setItem">Add to Cart</UButton>
      </div>
</template>