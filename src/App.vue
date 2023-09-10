<script setup lang="ts">
import { ServerIcon } from '@heroicons/vue/24/solid';
import List from './components/List.vue'
import RowCards from './components/RowCards.vue'

import { Bar } from 'vue-chartjs'
import { Chart as ChartJS, Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale } from 'chart.js'

ChartJS.register(Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale)

// export default {
//   name: 'BarChart',
//   components: { Bar },
//   data() {
//     return {
//       chartData: {
//         labels: ['January', 'February', 'March'],
//         datasets: [{ data: [40, 20, 12] }]
//       },
//       chartOptions: {
//         responsive: true
//       }
//     }
//   }
// }

const data = {
  chartData: {
    labels: ['January', 'February', 'March'],
    datasets: [

      {
        label: 'Purchase Orders',
        backgroundColor: '#334be9',
        data: [440, 20, 12]
      },

      {
        label: 'Purchase Orders',
        backgroundColor: '#334be9',
        data: [48, 24, 11]
      },

    ]
  },
  chartOptions: {
    responsive: true,

    maintainAspectRatio: true
  }
}


const data1 = {
  chartData: {
    labels: ['January', 'February', 'March'],
    datasets: [
      {
        data: [40, 20, 12],
        label: 'Revenue',
        backgroundColor: '#334be9',
      },
      {
        data: [500, 25, 4],
        label: 'Revenue',
        backgroundColor: '#334be9',
      }


    ]
  },
  chartOptions: {
    responsive: true
  }
}



</script>

<template>
  <body>
    <div class="grid-container">
      <header class="header">
        <div class="logo">
          JULYS´S BLOG
        </div>
        <div class="header-left">
          <List />
        </div>
        <div class="header-right">
          <ServerIcon class="icon" />
          <ServerIcon class="icon" />
          <ServerIcon class="icon" />
        </div>
      </header>
      <main class="main-container">
        <RowCards />
        <div class="charts">
          <div class="charts-card">
            <p class="chart-title">
              Revenue vs Profit
            </p>
            <div id="bar-chart">

              <Bar colo :data="data1.chartData" :options="data1.chartOptions" />

            </div>
          </div>
          <div class="charts-card">
            <p class="chart-title">
              Purchase and Sales Orders
            </p>
            <div id="bar-chart">

              <Bar :data="data.chartData" :options="data.chartOptions" />

            </div>
          </div>
        </div>
      </main>

    </div>
  </body>
</template>

<style scoped>
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

.charts {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 20px;
}

.charts-card {
  background-color: #2c2e3a;
  margin-bottom: 20px;
  padding: 25px;
  box-sizing: border-box;
  -webkit-column-break-inside: avoid;
  border-radius: 5px;
  box-shadow: 0px 6px 7px -4px rgba(0, 0, 0, 0.2);
}

.chart-title {
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 22px;
  font-weight: 600;
  color: #fff;
}

@media screen and (max-width: 962px) {
  .charts {
    grid-template-columns: 1fr;
    margin-top: 30px;
  }

  .header-left {
    display: none;
  }

  #bar-chart {
    width: 100%;
  }
}
</style>
