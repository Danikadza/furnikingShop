<script setup lang="ts">
import { computed } from 'vue'

const props = defineProps<{
    type: string
}>()

const iconType = computed(() => {
    if (props.type === 'new') {
        return "New"

    }
    if (props.type === 'sale') {
        return "Sale"

    }
})

</script>

<template>
    <div class="newIcon" :class="[iconType]">
        {{iconType}}
    </div>
</template>

<style>
.newIcon {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 44px;
    height: 20px;
    border-radius: 5px;
    font-size: 12px;
    color: white;
}

.New {
    background: #00B7F1;
}

.Sale {
    background: #7AC751;
}
</style>