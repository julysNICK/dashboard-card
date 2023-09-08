<script setup lang="ts">
import { SquaresPlusIcon, BuildingStorefrontIcon, HandThumbUpIcon, ServerIcon, MusicalNoteIcon } from '@heroicons/vue/24/solid';
defineProps({
  title: String,
  icon: String,

});

</script>

<template>
  <li class="list-item">
    <a href="#">
      <span class="material-icons-outlined">
        <SquaresPlusIcon v-if="icon === 'SquaresPlusIcon'" class="icon" />
        <BuildingStorefrontIcon v-if="icon === 'BuildingStorefrontIcon'" class="icon" />
        <HandThumbUpIcon v-if="icon === 'HandThumbUpIcon'" class="icon" />
        <ServerIcon v-if="icon === 'ServerIcon'" class="icon" />
        <MusicalNoteIcon v-if="icon === 'MusicalNoteIcon'" class="icon" />
      </span> {{ title }}
    </a>
  </li>
</template>


<style scoped>
.list-item {
  display: inline;
  padding: 20px 20px 20px 20px;
}

a {
  color: #fff;
  text-decoration: none;
}

.icon {
  width: 30px;
  height: 30px;
  color: #fff;
}

.material-icons-outlined {
  vertical-align: middle;
  line-height: 1px;
}
</style>