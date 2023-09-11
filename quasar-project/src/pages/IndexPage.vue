<template>
  <q-page class="row items-center justify-evenly">
    {{ testing }}
  </q-page>
</template>

<script setup lang="ts">
const testing = process.env.test;
</script>
