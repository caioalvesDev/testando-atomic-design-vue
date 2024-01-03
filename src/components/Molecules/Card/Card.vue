<script setup lang="ts">

</script>

<template>
  <div class="card">
   <slot />
  </div>
</template>



<style scoped>

.card {
  background-color: white;
  border-radius: 0.5rem;
  border: solid 1px rgb(229 231 235);
  width: 100%;
  display: flex;
  flex-direction: column;
  gap: 0.8rem;
  padding: 0.7rem;
  box-shadow: 0 1px 3px 0 rgb(0 0 0 / 0.1), 0 1px 2px -1px rgb(0 0 0 / 0.1);
}

</style>