<script setup lang="ts">
import ColorToggle from "@/components/ColorToggle.vue";

const links = [
  { to: '/', label: 'Home', exact: true },
  { to: '/pathfinding', label: 'Pathfinding', exact: false },
  { to: '/sorting', label: 'Sorting', exact: false },
  { to: '/searching', label: 'Searching', exact: false },
  { to: '/convolution', label: 'Convolution', exact: false },
  { to: '/digit-recognizer', label: 'Digits', exact: false },
]
</script>

<template>
  <header class="w-full bg-background border-b border-border">
    <div class="max-w-6xl mx-auto px-6 py-4 flex items-center justify-between">
      <div class="flex items-center gap-6">
        <RouterLink to="/" class="text-2xl font-bold tracking-tight">AlgoView</RouterLink>
        <nav class="flex items-center gap-1">
          <RouterLink
            v-for="link in links"
            :key="link.to"
            :to="link.to"
            class="px-3 py-2 rounded-md text-sm font-medium text-muted-foreground transition-colors hover:text-foreground hover:bg-accent"
            :active-class="link.exact ? '' : 'bg-accent text-foreground'"
            :exact-active-class="link.exact ? 'bg-accent text-foreground' : ''"
          >
            {{ link.label }}
          </RouterLink>
        </nav>
      </div>

      <ColorToggle />
    </div>
  </header>
</template>
