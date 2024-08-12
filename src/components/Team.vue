<script setup lang="ts">
    import Card from "./Card.vue";
</script>
<template>
    <div class="grid-container">
        <Card></Card>
        <Card></Card>
        <Card></Card>
        <Card></Card>
        <Card></Card>
        <Card></Card>
        <Card></Card>
        <Card></Card>
        <Card></Card>
    </div>
</template>
<style scoped>
.grid-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    width: 100%;
    gap: 22px;
    padding-top: 30px;
}</style>