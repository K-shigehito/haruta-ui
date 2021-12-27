<script setup lang="ts">
import Stack from './Stack.vue';
const list = [
  {
    name: 'mugi',
  },
  {
    name: 'hana',
  },
  {
    name: 'jigoro',
  },
];
</script>

<template>
  <Stack :space="2" class="bg-teal-200">
    <div v-for="item in list" :key="item.name" class="bg-gray-100">
      {{ item.name }}
    </div>
    <Stack :space="1" class="bg-blue-200">
      <div class="bg-gray-300">test</div>
      <div class="bg-gray-300">test</div>
    </Stack>
  </Stack>
</template>

<style></style>
