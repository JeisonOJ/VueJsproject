<template>
    <div class="grid-container-connection">
      <CardConnection></CardConnection>
      <CardConnection></CardConnection>
      <CardConnection></CardConnection>
      <CardConnection></CardConnection>
      <CardConnection></CardConnection>
      <CardConnection></CardConnection>
    </div>
  </template>
  
  <script setup lang="ts">
  import CardConnection from "./CardConnection.vue";
  </script>
  
  <style scoped>
  .grid-container-connection {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    width: 100%;
    gap: 22px;
    padding-top: 30px;
  }
  </style>