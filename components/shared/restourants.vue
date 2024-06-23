<script setup lang="ts">
import { restourants } from '~/constants'
</script>

<template>
    <div class="w-[250px] flex gap-4 flex-col flex-wrap  justify-between mx-4 shadow-md rounded-xl"
        v-for="(item, index) in restourants" :key="index">
        <img :src="item.img" :alt="item.name" class="w-full">
        <div class="p-3">
            <h4 class="text-[#363853] font-semibold">{{ item.name }}</h4>
        <div class="flex gap-3 items-center justify-between">
            <span class="text-xs">
                <Icon name="tabler:clock-hour-3" />{{ item.hour }}
            </span>
            <UButton color="orange" size="sm" class="rounded-full rounded-br-none px-4"><Icon name="material-symbols:arrow-forward" color="white"/></UButton>
        </div>
        </div>
    </div>
</template>