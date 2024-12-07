<script setup lang="ts">
const tasks = [
  { name: 'Water tomatoes', due: 'Today', priority: 'High' },
  { name: 'Harvest basil', due: 'Tomorrow', priority: 'Medium' },
  { name: 'Add fertilizer', due: 'Next week', priority: 'Low' },
]
</script>

<template>
  <div class="bg-white p-6 rounded-lg shadow">
    <h2 class="text-xl font-bold mb-4">Garden Tasks</h2>
    <div class="space-y-3">
      <div v-for="task in tasks" :key="task.name" 
           class="flex items-center justify-between p-3 bg-gray-50 rounded">
        <div>
          <h3 class="font-medium">{{ task.name }}</h3>
          <p class="text-sm text-gray-600">Due: {{ task.due }}</p>
        </div>
        <span :class="{
          'px-2 py-1 rounded text-xs font-medium': true,
          'bg-red-100 text-red-800': task.priority === 'High',
          'bg-yellow-100 text-yellow-800': task.priority === 'Medium',
          'bg-green-100 text-green-800': task.priority === 'Low'
        }">
          {{ task.priority }}
        </span>
      </div>
    </div>
  </div>
</template>
