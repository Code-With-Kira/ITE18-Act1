<script setup lang="ts">
const route = useRoute()

const links = [
  { label: 'Home', to: '/' },
  { label: 'Profile', to: '/profile' },
]
</script>

<template>
  <header class="border-b border-slate-200 bg-white/95">
    <nav class="mx-auto flex min-h-16 max-w-6xl items-center justify-between px-5 sm:px-8" aria-label="Main navigation">
      <NuxtLink to="/" class="text-lg font-bold tracking-tight text-slate-900">
        <span class="text-blue-600">L</span>aurence Egay
      </NuxtLink>

      <div class="flex items-center gap-1 rounded-full bg-slate-100 p-1">
        <NuxtLink
          v-for="link in links"
          :key="link.to"
          :to="link.to"
          class="rounded-full px-4 py-2 text-sm font-semibold transition focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-blue-600"
          :class="route.path === link.to
            ? 'bg-white text-blue-700 shadow-sm'
            : 'text-slate-600 hover:text-slate-950'"
        >
          {{ link.label }}
        </NuxtLink>
      </div>
    </nav>
  </header>
</template>
