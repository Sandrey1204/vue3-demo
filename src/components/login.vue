<script setup>
import { ref } from "vue";
import { onClickOutside } from "@vueuse/core";
defineProps({
  msg: String,
});
</script>

<template>
  <div ref="login">我在登录</div>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
