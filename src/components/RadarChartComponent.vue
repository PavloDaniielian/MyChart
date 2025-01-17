<template>
  <div style="width: 500px; height: 500px; margin: auto;">
    <RadarChart :chart-data="chartData" :options="chartOptions" />
  </div>
</template>

<script>
import { Chart as ChartJS, RadialLinearScale, PointElement, LineElement, Tooltip, Legend } from "chart.js";
import { Radar } from "vue-chartjs";

// Register necessary Chart.js components
ChartJS.register(RadialLinearScale, PointElement, LineElement, Tooltip, Legend);

export default {
  name: "RadarChartComponent",
  components: {
    RadarChart: Radar,
  },
  data() {
    return {
      chartData: {
        labels: ["Strength", "Skill", "Speed", "Agility", "Stamina"],
        datasets: [
          {
            label: "Player Stats",
            data: [65, 75, 70, 80, 60],
            backgroundColor: "rgba(75, 192, 192, 0.2)",
            borderColor: "rgba(75, 192, 192, 1)",
            borderWidth: 2,
          },
        ],
      },
      chartOptions: {
        responsive: true,
        plugins: {
          legend: {
            position: "top",
          },
        },
        scales: {
          r: {
            beginAtZero: true,
          },
        },
      },
    };
  },
};
</script>