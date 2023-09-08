<script setup lang="ts">
import ListItem from './ListItem.vue';
</script>

<template>
  <ul class="list">
    <ListItem title="Products" icon="SquaresPlusIcon" />
    <ListItem title="Reports" icon="HandThumbUpIcon" />
    <ListItem title="Settings" icon="ServerIcon" />
    <ListItem title="Settings" icon="ServerIcon" />
  </ul>
</template>
<style scoped>
.list {
  list-style-type: none;
}
</style>
