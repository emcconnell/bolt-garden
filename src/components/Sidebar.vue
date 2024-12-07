<script setup lang="ts">
import { HomeIcon, ChartBarIcon, CalendarIcon, CogIcon } from '@heroicons/vue/24/outline'

const menuItems = [
  { name: 'Dashboard', icon: HomeIcon },
  { name: 'Statistics', icon: ChartBarIcon },
  { name: 'Schedule', icon: CalendarIcon },
  { name: 'Settings', icon: CogIcon },
]
</script>

<template>
  <aside class="w-64 bg-green-800 text-white p-6">
    <h2 class="text-2xl font-bold mb-8">GardenTracker</h2>
    <nav>
      <ul class="space-y-4">
        <li v-for="item in menuItems" :key="item.name">
          <a href="#" class="flex items-center space-x-2 p-2 hover:bg-green-700 rounded">
            <component :is="item.icon" class="w-5 h-5" />
            <span>{{ item.name }}</span>
          </a>
        </li>
      </ul>
    </nav>
  </aside>
</template>
