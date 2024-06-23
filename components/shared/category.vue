<script setup lang="ts">
import {categorys} from '~/constants'
</script>
<template>
    <div class="w-[210px] flex gap-4 my-4 items-center justify-center mx-4 shadow-md rounded-lg p-3 hover:text-white hover:bg-orange-400 ease-in-out duration-150" v-for="(item, index) in categorys" :key="index">
        <Icon :name="item.icon" size="25"/>
        <h4>{{ item.name }}</h4>
      </div>
</template>