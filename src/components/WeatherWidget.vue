<script setup lang="ts">
const weather = {
  temp: '22°C',
  condition: 'Sunny',
  humidity: '65%',
  rainfall: '0mm'
}
</script>

<template>
  <div class="bg-white p-6 rounded-lg shadow">
    <h2 class="text-xl font-bold mb-4">Weather</h2>
    <div class="grid grid-cols-2 gap-4">
      <div class="text-center p-3 bg-blue-50 rounded">
        <div class="text-2xl font-bold">{{ weather.temp }}</div>
        <div class="text-sm text-gray-600">Temperature</div>
      </div>
      <div class="text-center p-3 bg-blue-50 rounded">
        <div class="text-2xl font-bold">{{ weather.humidity }}</div>
        <div class="text-sm text-gray-600">Humidity</div>
      </div>
      <div class="text-center p-3 bg-blue-50 rounded">
        <div class="text-2xl font-bold">{{ weather.condition }}</div>
        <div class="text-sm text-gray-600">Condition</div>
      </div>
      <div class="text-center p-3 bg-blue-50 rounded">
        <div class="text-2xl font-bold">{{ weather.rainfall }}</div>
        <div class="text-sm text-gray-600">Rainfall</div>
      </div>
    </div>
  </div>
</template>
