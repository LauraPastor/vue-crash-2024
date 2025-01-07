<template>
  <div :class="`${bg} p-6 rounded-lg shadow-md`">
    <h2 class="text-2xl font-bold">{{ title }}</h2>
    <p class="mt-2 mb-4">{{ subtitle }}</p>
    <RouterLink
      :to
      :class="`inline-block ${abg} text-white rounded-lg px-4 py-2
      hover:bg-gray-700`">
      {{ role }}
    </RouterLink>
  </div>
</template>
<script setup>
import { RouterLink } from 'vue-router';
import { defineProps } from 'vue';
defineProps({
  bg: {
    type: String,
    default: 'bg-gray-100',
  },
  title: {
    type: String,
    default: 'For Developers',
  },
  subtitle: {
    type: String,
    default: 'Browse our Vue jobs and start your career today',
  },
  abg: {
    type: String,
    default: 'bg-black',
  },
  role: {
    type: String,
    default: 'Browse Jobs',
  },
  to: {
    type: String,
    default: '/jobs',
  },
});
</script>
