<script lang="ts" setup>
const title = ref("Waiting for site data");

await new Promise((resolve) => {
  setTimeout(() => {
    title.value = "Site data loaded";
    resolve(true);
  }, 2000);
});
</script>

<template>
  <div>
    <div>
      This is a site
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