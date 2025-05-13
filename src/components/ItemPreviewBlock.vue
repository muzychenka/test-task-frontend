<script setup lang="ts">
defineProps<{
    name: string
}>()
</script>

<template>
    <div class="item-preview-block">{{ name }}</div>
</template>

<style scoped>
.item-preview-block {
    width: 15rem;
    min-height: 15rem;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 2rem;
    border: 0.2rem solid #000;
    padding: 0.25rem;
}
</style>
