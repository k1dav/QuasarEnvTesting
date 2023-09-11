<template>
  <q-page class="row items-center justify-evenly">
    {{ testing }}
    <br/>
    {{ noTesting }}
  </q-page>
</template>

<script setup lang="ts">
const testing = process.env.test;
const noTesting = process.env.no_test || 'null';
</script>
