<script setup lang="ts">
import PlantList from './PlantList.vue'
import WeatherWidget from './WeatherWidget.vue'
import TaskList from './TaskList.vue'
import GardenStats from './GardenStats.vue'
</script>

<template>
  <main class="flex-1 p-6 overflow-auto">
    <h1 class="text-3xl font-bold text-gray-800 mb-6">My Garden Dashboard</h1>
    
    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
      <WeatherWidget />
      <GardenStats />
      <PlantList />
      <TaskList />
    </div>
  </main>
</template>
