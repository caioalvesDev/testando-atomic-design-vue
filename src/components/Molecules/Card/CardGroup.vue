<script setup lang="ts" >
import type { CSSProperties } from "vue";
interface IProps {
  list: [] | any;
  ui?: CSSProperties;
  direction?: "row" | "column";
}

const props = withDefaults(defineProps<IProps>(), {
  direction: "row",
});
</script>

<template>
  <div v-for="(item, index) in props.list" :key="index">
    <slot v-bind="item" />
  </div>
</template>

<style scoped>

</style>
