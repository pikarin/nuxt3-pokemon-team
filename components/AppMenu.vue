<script lang="ts" setup>
interface NavMenu {
  label: string
  url: string
}

defineEmits(['close'])

const navMenus: NavMenu[] = [
  {
    label: 'Teams',
    url: '/teams',
  },
  {
    label: 'My Favorite Pokemon',
    url: '/favourites',
  },
]
</script>

<template>
  <nav class="border-t border-gray-100 py-4">
    <ul>
      <li v-for="(menu, index) in navMenus" :key="index">
        <a
          href="#"
          class="block p-2 mx-2 border border-transparent hover:border-blue-300 rounded-md"
          @click="$emit('close')"
        >
          {{ menu.label }}
        </a>
      </li>
    </ul>
  </nav>
</template>
