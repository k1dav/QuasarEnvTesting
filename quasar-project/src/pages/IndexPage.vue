<template>
  <q-page class="row items-center justify-evenly">
    {{ testing }}
    <br/>
    {{ noTesting }}
    <br/>
    {{ condTest }}
  </q-page>
</template>

<script setup lang="ts">
const testing = process.env.test;
const condTest = process.env.condTest;
const noTesting = process.env.no_test || 'null';
</script>
