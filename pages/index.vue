<script lang="ts" setup>
const { data }: { data: any } = await useFetch(
  'https://pokeapi.co/api/v2/pokemon/'
)
</script>

<template>
  <div>
    <h1>Pokemon</h1>
    <ul>
      <li v-for="pokemon in data.results" :key="pokemon.name">
        {{ pokemon.name }}
      </li>
    </ul>
  </div>
</template>
