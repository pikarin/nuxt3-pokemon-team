<script lang="ts" setup>
const { POKE_API_URL } = useRuntimeConfig()
const props = defineProps({
  limit: {
    type: Number,
    default: 20,
  },
})

const randomOffset = () => Math.floor(Math.random() * 1000)

const { data }: { data: any } = await useFetch(
  `${POKE_API_URL}/pokemon?limit=${props.limit}&offset=${randomOffset()}`
)
</script>

<template>
  <ul>
    <li v-for="pokemon in data.results" :key="pokemon.name">
      {{ pokemon.name }}
    </li>
  </ul>
</template>
