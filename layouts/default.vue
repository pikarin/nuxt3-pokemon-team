<template>
  <article>
    <AppHeader />
    <main>
      <slot />
    </main>
    <AppFooter />
  </article>
</template>

<style scoped>
article {
  min-height: 100vh;
  display: grid;
  grid-template-rows: auto 1fr auto;
  grid-template-columns: 100%;
}
</style>
