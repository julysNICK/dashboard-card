<script setup lang="ts">
import { SquaresPlusIcon, BuildingStorefrontIcon, HandThumbUpIcon, ServerIcon, MusicalNoteIcon } from '@heroicons/vue/24/solid';
import Card from './components/Card.vue';




</script>

<template>
  <!-- <header>
    <meta charset="utf-8">
    <title>Vue 3 + Vite + TypeScript</title>
  </header> -->

  <body>
    <div class="grid-container">
      <header class="header">
        <div class="logo">
          JULYS´S BLOG
        </div>

        <div class="header-left">
          <ul class="list">
            <li class="list-item">
              <a href="#">
                <span class="material-icons-outlined">
                  <SquaresPlusIcon class="icon" />
                </span> DASHBOARD
              </a>
            </li>
            <li class="list-item">
              <a href="#">
                <span class="material-icons-outlined">
                  <BuildingStorefrontIcon class="icon" />
                </span> PRODUCTS
              </a>
            </li>
            <li class="list-item">
              <a href="#">
                <span class="material-icons-outlined">
                  <HandThumbUpIcon class="icon" />
                </span> REPORTS
              </a>
            </li>

            <li class="list-item">
              <a href="#">
                <span class="material-icons-outlined">
                  <ServerIcon class="icon" />
                </span> SETTINGS
              </a>
            </li>
          </ul>
        </div>

        <div class="header-right">
          <ServerIcon class="icon" />
          <ServerIcon class="icon" />
          <ServerIcon class="icon" />

        </div>
      </header>


      <main class="main-container">
        <div class="main-cards">
          <Card color="red" title="PRODUCTS" value=193 />
          <Card color="blue" title="ALERTS" value=193 />
          <Card color="green" title="IMPORTANTS" value=193 />
          <Card color="blue" title="ALERTS" value=193 />

        </div>
      </main>

    </div>
  </body>
</template>

<style scoped>
.material-icons-outlined {
  vertical-align: middle;
  line-height: 1px;

}

.text-primary {
  color: #fff;
}

.text-blue {
  color: #334be9;
}

.text-red {
  color: #e3342f;
}

.background-red {
  background-color: #e3342f;
}

.background-green {
  background-color: #38c172;
}

.background-blue {
  background-color: #334be9;
}

.text-orange {
  color: #ff7e00;
}

.background-orange {
  background-color: #ff7e00;
}

.grid-container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  grid-template-rows: 0.2fr 3fr;
  grid-template-areas:
    "header header header header"
    "main main main main";
  height: 100vh;
}

.header {
  grid-area: header;
  height: 70px;
  background-color: #334be9;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 30px 0 30px;
  box-shadow: 0px 6px 7px -4px rgba(0, 0, 0, 0.2);

}

.logo {
  font-size: 20px;
  font-weight: 700;
  color: #fff;
}

.list {
  list-style-type: none;
}

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

.main-container {
  grid-area: main;
  overflow-y: auto;
  padding: 20px 20px;

}

.main-title {
  display: flex;
  justify-content: space-between;
}

.main-title>p {
  font-size: 20px;
}

.main-cards {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 20px;
  margin: 20px 0px;

}
</style>
