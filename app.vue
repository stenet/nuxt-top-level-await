<script setup lang="ts">
const title = ref("Waiting for something");

await new Promise((resolve) => {
  setTimeout(() => {
    title.value = "Here we are";
    resolve(true);
  }, 2000);
});
</script>

<template>
  <div>
    <nav>
      <NuxtLink to="/">Index</NuxtLink>
      <NuxtLink to="/page">Page</NuxtLink>
      <NuxtLink to="/site">Site</NuxtLink>
      <NuxtLink to="/failure">Failure</NuxtLink>
    </nav>
    <div>
      {{ title }}
    </div>
    <NuxtLoadingIndicator />
    <TheLoader/>

    <NuxtPage/>
  </div>
</template>

<style>
nav {
  display: flex;
  gap: .5rem;
}
</style>