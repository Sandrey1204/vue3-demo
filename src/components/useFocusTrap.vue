<script setup>
import { ref } from "vue";
import { useFocusTrap } from "@vueuse/core";

const container = ref(null);
useFocusTrap(container, { immediate: true });
</script>

<template>
  <div>
    <button tab-index="-1">Can't click me</button>
    <div class="container" ref="container">
      <button tab-index="-1">Inside the trap</button>
      <button tab-index="-1">Can't break out</button>
      <button tab-index="-1">Stuck here forever</button>
    </div>
    <button tab-index="-1">Can't click me</button>
  </div>
</template>

<style>
body {
  font-family: sans-serif;
}

button {
  margin: 8px 0;
  padding: 12px 16px;
  background: slategrey;
  color: white;
  font-weight: bold;
  font-size: 18px;
  border: none;
  border-radius: 4px;
}

button:focus {
  outline: skyblue solid 6 px;
}

.container {
  display: flex;
  flex-direction: column;
  border: 2px solid gray;
  border-radius: 6px;
  margin: 16px 0;
  padding: 4px 8px;
}
</style>
