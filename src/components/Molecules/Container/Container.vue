<script setup lang="ts">
type Size = "none" | "sm" | "md" | "lg" | "xl" | "2xl";
interface IProps {
  size?: Size;
}

const props = withDefaults(defineProps<IProps>(), {
  size: "lg",
});
</script>

<template>
  <div :class="[$style.container, $style[props.size === '2xl' ? `_${props.size}` : props.size]]">
    <slot />
  </div>
</template>

<style module scoped>
.container {
  margin: 0 auto;
}

.nome {
  width: 100%;
}
.sm {
  max-width: 640px;
}
.md {
  max-width: 768px;
}
.lg {
  max-width: 1024px;
}
.xl {
  max-width: 1280px;
}
._2xl {
  max-width: 1536px;
}
</style>
