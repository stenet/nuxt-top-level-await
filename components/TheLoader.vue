<script lang="ts" setup>
const visible = ref(false);

const nuxtApp = useNuxtApp();
nuxtApp.hook("page:start", () => {
  visible.value = true;
});
nuxtApp.hook("page:finish", () => {
  visible.value = false;
});

onBeforeUnmount(() => {
  visible.value = false;
});
</script>

<template>
  <Transition name="loader">
    <div v-if="visible" class="the-loader">
      Loading
    </div>
  </Transition>
</template>

<style>
.the-loader {
  position: fixed;
  display: flex;
  justify-content: center;
  align-items: center;
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  z-index: 99;
  background-color: rgb(255 255 255 / .8);
}

.loader-enter-from, .loader-leave-to {
  opacity: 0;
}
.loader-enter-active {
  transition: opacity 300ms ease-in-out;
}

.loader-leave-active {
  transition: opacity 150ms ease-in-out;
}
</style>