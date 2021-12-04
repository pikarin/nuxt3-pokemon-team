<script lang="ts" setup>
import { MenuIcon, PlusCircleIcon } from '@heroicons/vue/outline'

const show = ref(false)

const toggle = () => {
  show.value = !show.value
}
</script>

<template>
  <header class="shadow">
    <div class="container py-4">
      <nav class="flex items-center justify-between">
        <div class="w-10">
          <button @click="toggle">
            <MenuIcon class="h-6 w-6" />
          </button>
        </div>
        <span class="text-blue-500 text-2xl">Pokémon</span>
        <div class="w-10">
          <button class="text-blue-500">
            <PlusCircleIcon class="h-8 w-8" />
          </button>
        </div>
      </nav>
    </div>

    <AppMenu v-if="show" @close="toggle" />
  </header>
</template>
