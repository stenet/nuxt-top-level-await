<script lang="ts" setup>
function onClearErrorClick() {
  clearError({
    redirect: "/"
  });
}
</script>

<template>
  <div>
    <div>
      Ooops
    </div>
    <div>
      <button @click="onClearErrorClick()">Clear error</button>
    </div>
  </div>
</template>

<style lang="less">
</style>