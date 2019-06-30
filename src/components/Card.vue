<template>
  <div class="p-8 rounded-lg bg-white shadow-lg">
    <div v-if="!loaded" class="p-6 text-xl text-gray-600 font-bold text-center">
      Loading...
    </div>
    <Chart v-if="loaded" :chartData="chartData" :options="options" />
  </div>
</template>

<script>
import Chart from "./Chart.vue";
import data from "../data/data.js";

export default {
  name: "Card",
  components: {
    Chart
  },
  data: () => ({
    loaded: false,
    chartData: null,
    options: {
      responsive: true,
      maintainAspectRatio: false,
      scales: {
        xAxes: [
          {
            scaleLabel: {
              display: true,
              labelString: "Months"
            }
          }
        ],
        yAxes: [
          {
            id: "cards-y-axis",
            offset: true,
            gridLines: {
              display: false
            },
            scaleLabel: {
              display: true,
              labelString: "Amount of Active Cards",
              fontColor: "#285e61"
            }
          },
          {
            id: "fraud-y-axis",
            position: "right",
            offset: true,
            gridLines: {
              display: false
            },
            scaleLabel: {
              display: true,
              labelString: "Amount of Money Lost ($)",
              fontColor: "#9b2c2c"
            }
          }
        ]
      }
    }
  }),
  mounted() {
    this.loadChartData();
  },
  methods: {
    loadChartData() {
      this.loaded = false;
      setTimeout(() => {
        this.chartData = data;
        this.loaded = true;
      }, 500);
    }
  }
};
</script>

<style scoped></style>
