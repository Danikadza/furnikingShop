<script setup lang="ts">
import {computed} from 'vue'

const props = defineProps <{
type: string
size: string
}>()

const buttonType = computed ( () => {
    if (props.type === 'primary') {
        return "button__primary"
    }
    if (props.type === 'text_primary') {
        return "button__textPrimary"
    }
    if (props.type === 'text_secondary') {
        return "button__textSecondary"
    }
    if (props.type === 'text_secondaryGreen') {
        return "button__textSecondaryGreen"
    }
})

const buttonSize = computed (() => {
    if (props.size === 'large') {
    return "button__large"
  }
  if (props.size === 'small') {
    return "button__small"
  }
  return "button__default"
})
</script>

<template>
<button class="button"
:class="[buttonType, buttonSize]"
>
    <slot></slot>
    </button>
</template>

<style>
.button {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 10px 18px;
    border-radius: 5px;
    cursor: pointer;
    box-sizing: border-box;
    font-family: 'Mulish';
    font-style: normal;
    font-weight: 700;
    font-size: 16px;
    line-height: 20px;
}

.button__primary {
    color: #fff;
    background-color: #7AC751;
}

.button__textPrimary {
    padding: 0px;
    color: #555555;
    background-color: white;
    border: none;
    box-shadow: none;
}

.button__textSecondary {
    padding: 0px;
    color: #C2C2C2;
    background-color: white;
    border: none;
    box-shadow: none;
}

.button__textSecondaryGreen {
    padding: 0px;
    color:#7AC751;
    background-color: white;
    border: none;
    box-shadow: none;
}

.button__default {
    height: 40px;
    font-size: 16px;
}

.button__small {
    height: 20px;
    font-size: 14px;
}

.button__large {
    height: 30px;
    font-size: 24px;
}
</style>