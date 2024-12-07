<script setup lang="ts">
const plants = [
  { name: 'Tomatoes', health: 'Good', nextWatering: 'Today' },
  { name: 'Basil', health: 'Excellent', nextWatering: 'Tomorrow' },
  { name: 'Peppers', health: 'Needs attention', nextWatering: 'Today' },
]
</script>

<template>
  <div class="bg-white p-6 rounded-lg shadow">
    <h2 class="text-xl font-bold mb-4">My Plants</h2>
    <div class="space-y-4">
      <div v-for="plant in plants" :key="plant.name" 
           class="flex items-center justify-between p-3 bg-gray-50 rounded">
        <div>
          <h3 class="font-medium">{{ plant.name }}</h3>
          <p class="text-sm text-gray-600">Health: {{ plant.health }}</p>
        </div>
        <div class="text-sm text-gray-500">
          Water: {{ plant.nextWatering }}
        </div>
      </div>
    </div>
  </div>
</template>
