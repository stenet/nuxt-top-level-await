<script lang="ts" setup>
definePageMeta({
  keepalive: true
});

const title = ref("Waiting for page data");

await new Promise((resolve) => {
  setTimeout(() => {
    title.value = "Page data loaded";
    resolve(true);
  }, 2000);
});
</script>

<template>
  <div>
    <div>
      This is a page
    </div>
    <div>
      {{ title }}
    </div>
    <div>
      <input type="text">
    </div>
  </div>
</template>

<style lang="less">
</style>