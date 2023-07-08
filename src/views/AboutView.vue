<script setup lang="ts">
import Button from '@/components/Button.vue'
import Product from  '@/components/Product.vue'
import Trending from  '@/components/Trending.vue'
</script>


<template>
  <div class = "page">
  <div class="about">
    <Button type="primary" size="large">BUTTON</Button>
    <Button type="primary" size="default">BUTTON</Button>
    <Button type="primary" size="small">BUTTON</Button>
    <Button type="text_primary" size="small">BUTTON</Button>
    <Button type="text_secondaryGreen" size="small">BUTTON</Button>
  </div>
  <div>
    <Product type-new="new"  category="CHAIR" name="Minimal chair" price="$120" sale-price="$150" review="4">
      <img src=../product1.png />
    </Product>
  </div>
  <div class="trending">
    <Trending></Trending>
  </div>
</div>
</template>

<style>
.page {
  display: flex;
  flex-direction: column;
}
.about {
  display: flex;
  gap: 10px;
}

</style>
