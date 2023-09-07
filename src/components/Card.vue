<script setup lang="ts">
import { HandThumbUpIcon } from '@heroicons/vue/24/solid';

defineProps({
  title: String,
  icon: String,
  color: String,
  value: String,
});


const changedBackgroundColor = (color?: String) => {
  if (color === 'red') {
    return 'background-red';
  } else if (color === 'green') {
    return 'background-green';
  } else if (color === 'blue') {
    return 'background-blue';
  }
};


</script>
<template>
  <div class="card">
    <div class="card-inner">

      <p>{{ title }}</p>

      <div class="icon-card icon-shape text-primary" :class="changedBackgroundColor(color)">
        <span class="material-icons-outlined">
          <HandThumbUpIcon class="icon" />
        </span>
      </div>
    </div>
    <span class="text-primary">{{ value }}</span>
  </div>
</template>

<style scoped>
.background-red {
  background-color: #e3342f;
}

.background-green {
  background-color: #38c172;
}

.background-blue {
  background-color: #334be9;
}

.icon {
  width: 30px;
  height: 30px;
  color: #fff;
}

.card {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  padding: 25px;
  background-color: #2c2e3a;
  box-sizing: border-box;
  border-radius: 5px;
  box-shadow: 0px 6px 7px -4px rgba(0, 0, 0, 0.2);
}

.card:first-child {
  border-left: 5px solid #334be9;
}

.card:nth-child(2) {
  border-left: 5px solid #38c172;
}

.card:nth-child(3) {
  border-left: 5px solid #ff7e00;
}

.card:nth-child(4) {
  border-left: 5px solid #e3342f;
}

.card>span {
  font-size: 30px;
  font-weight: 700;
}


.card-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.card-inner>p {
  font-size: 23px;
  font-weight: 700;
}

.card-inner>span {}

.icon-card {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>