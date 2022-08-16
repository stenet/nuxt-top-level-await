<script lang="ts" setup>
definePageMeta({
  keepalive: true
});

await new Promise((resolve, reject) => {
  setTimeout(() => {
    showError({
      statusCode: 400
    });
    
    reject();
  }, 1000);
});
</script>

<template>
  <div>
    An error ocurred.
  </div>
</template>

<style lang="less">
</style>