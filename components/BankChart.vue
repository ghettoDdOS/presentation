<script setup lang="ts">
import {
  BarElement,
  CategoryScale,
  Chart as ChartJS,
  Legend,
  LinearScale,
  Title,
  Tooltip,
} from 'chart.js'
import { Bar } from 'vue-chartjs'

ChartJS.register(Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale)

const chartData = {
  labels: [
    'Райффайзенбанк',
    'ВТБ',
    'Тинькофф Банк',
    'Уральский Банк Реконструкции и Развития',
    'МТС Банк',
    'Русский Стандарт',
    'Альфа-Банк',
    'Росбанк',
    'Банк Открытие',
    'Промсвязьбанк',
    'Россельхозбанк',
    'Хоум Кредит Банк',
    'Газпромбанк',
    'Совкомбанк',
    'Ак Барс',
    'СберБанк',
    'Почта Банк',
    'Банк Уралсиб',
    'Московский Кредитный Банк',
    'ЮниКредит Банк',
  ],
  datasets: [
    {
      label: 'Коммуникации',
      backgroundColor: '#1F2544',
      data: [
        24, 26, 18, 21.3, 18, 19.3, 11, 17.3, 11, 15, 30, 18, 11, 9, 14, 16, 11,
        14.3, 9, 11,
      ],
    },
    {
      label: 'Платежные сервисы и технологии',
      backgroundColor: '#474F7A',
      data: [
        37.1, 39.1, 39.7, 32.1, 38.3, 36.8, 38.2, 39.5, 39, 39.1, 28.4, 29.5,
        36.1, 37.4, 37, 39.5, 38.2, 33.3, 38.2, 35.4,
      ],
    },
    {
      label: 'Оформление продуктов',
      backgroundColor: '#81689D',
      data: [
        20, 15, 20, 20, 15, 15, 15, 20, 20, 15, 10, 20, 20, 20, 20, 15, 10, 15,
        15, 15, 15,
      ],
    },
  ],
}
const chartOptions = {
  responsive: true,
}
</script>

<template>
  <Bar
    id="bank-chart"
    :options="chartOptions"
    :data="chartData"
  />
</template>
