<template>
  <h1>Product</h1>
    <main class="wrapper">
      <div class="card-container">
         <ProductCard
        class="card"
        v-for="(product, index) in inventory.slice(0,6)"
        :key="product.id"
        :index="index"
        :product="product"
        :addToCart="addToCart"
        />
      </div>
    </main>
</template>

<script>
import ProductCard from '@/components/ProductCard.vue'

export default {
  props: ['inventory', 'addToCart'],
  components: {
    ProductCard
  }
}
</script>
