<script setup lang="ts">
import { useItemsStore } from '@/stores/items'
import CartPreviewBlock from '@/components/CartPreviewBlock.vue'
import ItemPreviewBlock from '@/components/ItemPreviewBlock.vue'
import ShowcaseBlock from '@/components/ShowcaseBlock.vue'

const itemsStore = useItemsStore()
</script>

<template>
    <main class="app">
        <div class="app__previews-wrapper">
            <cart-preview-block :selected-count="itemsStore.selectFromCart.length" />
            <item-preview-block name="" />
        </div>
        <div class="app__previews-wrapper">
            <showcase-block />
            <showcase-block />
        </div>
    </main>
</template>

<style scoped>
.app {
    width: max-content;
    margin: auto;
    font-size: 1.5rem;
    display: flex;
    justify-content: center;
    flex-direction: column;
    gap: 1.5rem;
}

.app__previews-wrapper {
    display: flex;
    justify-content: space-between;
    flex: 1;
}
</style>
