<script setup lang="ts">
import Button from '@/components/Button.vue'
import Product from '@/components/Product.vue'
</script>

<template>
    <div class="trending">
        <div class="trending__header">TRENDING</div>
        <div class="trending__category">
            <Button type="text_secondaryGreen" size="large">Top Products</Button>
            <Button type="text_secondaryGreen" size="large">New Arrivals</Button>
            <Button type="text_secondaryGreen" size="large">Best Sellers</Button>
        </div>
        <div class="trending__items">
            <Product type-new="new" category="CHAIR" name="Minimal chair" price="$120" sale-price="$150" review="4">
                <img src=../product1.png />
            </Product>
            <Product type-new="new" category="CHAIR" name="Minimal chair" price="$120" sale-price="$150" review="4">
                <img src=../product1.png />
            </Product>
            <Product type-new="new" category="CHAIR" name="Minimal chair" price="$120" sale-price="$150" review="4">
                <img src=../product1.png />
            </Product>
            <Product type-new="new" category="CHAIR" name="Minimal chair" price="$120" sale-price="$150" review="4">
                <img src=../product1.png />
            </Product>
            <Product type-new="new" category="CHAIR" name="Minimal chair" price="$120" sale-price="$150" review="4">
                <img src=../product1.png />
            </Product>
            <Product type-new="new" category="CHAIR" name="Minimal chair" price="$120" sale-price="$150" review="4">
                <img src=../product1.png />
            </Product>
            <Product type-new="new" category="CHAIR" name="Minimal chair" price="$120" sale-price="$150" review="4">
                <img src=../product1.png />
            </Product>
            <Product type-new="new" category="CHAIR" name="Minimal chair" price="$120" sale-price="$150" review="4">
                <img src=../product1.png />
            </Product>
        </div>
        <div class="trending__pages">
            <img src=../assets/Circle.svg />
            <img src=@/assets/Circle.svg />
        </div>
    </div>
</template>

<style>
.trending {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    width: 1170px;
    height: 1094px;
}

.trending__header{
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 36px;
    color: #555555;
}

.trending__category {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    gap: 60px;
}

.trending__items {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
    gap: 30px;
}

.trending__pages {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 30px;
}
</style>