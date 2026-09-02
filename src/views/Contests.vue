<script setup lang="ts">
import Timer from "./Timer.vue";

const dday = new Date("2026-09-26T12:00:00");
</script>

<template>
  <Timer :dday="dday"></Timer>
</template>

<style scoped>
</style>
