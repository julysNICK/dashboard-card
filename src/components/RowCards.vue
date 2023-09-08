<script setup lang="ts">
import Card from './Card.vue';
</script>

<template>
  <div class="main-cards">
    <Card color="red" title="PRODUCTS" value=193 />
    <Card color="blue" title="ALERTS" value=193 />
    <Card color="green" title="IMPORTANTS" value=193 />
    <Card color="blue" title="ALERTS" value=193 />
  </div>
</template>

<style scoped>
.main-cards {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 20px;
  margin: 20px 0px;

}
</style>