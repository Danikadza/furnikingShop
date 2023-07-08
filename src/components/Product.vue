<script setup lang="ts">
import { computed } from 'vue'
import New from  '@/components/New.vue'

const props = defineProps<{
    typeNew:string
    category: string
    name: string
    price: string
    salePrice: string
    review: string
}>()

</script>

<template>
    <div class="product">
        <New :type="typeNew" class="product_new">New</New>
        <div class="product__image">
            <slot></slot>
        </div>
        <div class="product__category">
            {{ category }}
        </div>
        <div class="product__name">
            {{ name }}
        </div>
        <div class="product_botBar">
            <div class="product__price">
                <div class="product__mainPrice">{{ price }}</div>
                <div class="product__salePrice">{{ salePrice }}</div>
            </div>
            <div class="product__review">
                5star
            </div>
        </div>
    </div>
</template>

<style>
.product {
    width: 270px;
    height: 387px;
}

.product_new {
    position: absolute;
}

.product_image {
    width: 270px;
    height: 287px;
}

.product__category {
    height: 18px;
    font-size: 14px;
    color: #757575B5;
}

.product__name {
    height: 28px;
    font-size: 20px;
    color: #555555;
}

.product_botBar {
    display: flex;
    justify-content: space-between;
}

.product__price {
    display: flex;
    flex-direction: row;
    gap: 5px;
}

.product__mainPrice{
height: 21px;
font-size: 18px;
color: #7AC751;
}

.product__salePrice{
    height: 21px;
    font-size: 18px;
    color: #CCCCCC;
    text-decoration: line-through;
}

</style>