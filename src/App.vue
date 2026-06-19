<script setup lang="ts">
import { Toaster } from 'vue-sonner'
import NavBar from '@/components/NavBar.vue'
</script>

<template>
  <NavBar />
  <div>
    <Toaster position="top-center" />
    <router-view />
  </div>
</template>
