<script setup lang="ts">
import CardItem from './CardItem.vue';
import type { Item } from '../types';
defineProps<{
  items: Item[]
}>()
</script>

<template>
  <section class="flex gap-[20px] flex-wrap max-w-[1500px] mx-auto">
    <CardItem v-for="item in items" :item="item" :key="item.id" />
  </section>
</template>

<style scoped>
</style>
