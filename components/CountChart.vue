<script setup lang="ts">
import {
  CategoryScale,
  Chart as ChartJS,
  Legend,
  LineElement,
  LinearScale,
  PointElement,
  Title,
  Tooltip,
} from 'chart.js'
import { Line } from 'vue-chartjs'

ChartJS.register(
  Title,
  Tooltip,
  Legend,
  LineElement,
  PointElement,
  CategoryScale,
  LinearScale
)

const chartData = {
  labels: [
    '2010',
    '2011',
    '2012',
    '2013',
    '2014',
    '2015',
    '2016',
    '2017',
    '2018',
    '2019',
  ],
  datasets: [
    {
      label: 'Юридические лица',
      borderColor: '#1F2544',
      data: [60.9, 67.9, 74.9, 83.8, 87.6, 90.2, 93.5, 96.4, 97.6, 98.4],
    },
    {
      label: 'Физические лица',
      borderColor: '#474F7A',
      data: [8.9, 18.2, 25.4, 29.2, 38.9, 66.2, 85.7, 86.2, 89.8, 93.2],
    },
  ],
}
const chartOptions = {
  responsive: true,
}
</script>

<template>
  <Line
    id="count-chart"
    :options="chartOptions"
    :data="chartData"
  />
</template>
