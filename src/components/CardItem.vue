<script setup lang="ts">
import type { Item } from '../types';
import { computed } from 'vue';
const props = defineProps<{
  item: Item
}>()

const descriptionIsArr = computed(() => Array.isArray(props.item.description))
</script>

<template>
  <a href="#"
    class="h-[336px] w-[437.5px] flex flex-col bg-white border border-gray-200 rounded-lg shadow md:flex-row md:max-w-xl hover:bg-gray-100">
    <img class="object-cover w-full rounded-t-lg h-96 md:h-auto md:w-48 md:rounded-none md:rounded-l-lg" :src="item.img"
      alt="">
    <div class="flex flex-col pt-[40px] pl-[34px] pr-[30px]">
      <h5 class="mb-2 text-2xl font-bold tracking-tight text-[#353844]">{{ item.title }}</h5>
      <ul class="my-[12px] text-[15px] list-disc ml-3" v-if="item.options">
        <li v-for="option in item.options">{{ option }}</li>
      </ul>
      <p v-if="descriptionIsArr" v-for="(description, index) in item.description" :key="index"
        class="mb-3 text-[15px] !font-extralight">{{ description }}</p>
      <p v-else class="mb-3 text-[15px] !font-extralight">{{ item.description }}</p>
    </div>
  </a>
</template>

