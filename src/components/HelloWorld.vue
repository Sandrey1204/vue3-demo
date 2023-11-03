<script setup>
import { ref } from "vue";
import { onClickOutside } from "@vueuse/core";
import useFocusTrap from "./useFocusTrap.vue";
import Login from "./login.vue";
defineProps({
  msg: String,
});
const count = ref(0);
const el = ref();
function close() {
  console.log("执行我了");
}
onClickOutside(el, close);
</script>

<template>
  <useFocusTrap></useFocusTrap>
  <p>
    Check out
    <a href="https://vuejs.org/guide/quick-start.html#local" target="_blank"
      >create-vue</a
    >, the official Vue + Vite starter
  </p>
  <p>
    Install
    <a href="https://github.com/vuejs/language-tools" target="_blank">Volar</a>
    in your IDE for a better DX
  </p>
  <p class="read-the-docs">Click on the Vite and Vue logos to learn more</p>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
