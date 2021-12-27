<script setup lang="ts">
import { computed } from '@vue/reactivity';

interface Props {
  space?: number;
}
const props = defineProps<Props>();
const spaceStyle = computed(() =>
  props.space ? { gap: `${props.space}em` } : ''
);
</script>

<template>
  <div class="flex flex-col justify-start" :style="spaceStyle">
    <slot />
  </div>
</template>

<style>
/* .stack * + * {
  margin-top: 1.7rem;
} */
</style>
