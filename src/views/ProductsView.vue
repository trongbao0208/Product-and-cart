<template>
  <main class="wrapper">
    <h1>Products</h1>
    <div class="card-container">
      <ProductCard
          v-for="(product, index) in inventory.slice(0, 6)"
          :key="product.id"
          class="card"
          :index="index"
          :product="product"
          :addToCart="addToCart"
        />
    </div>
  </main>
</template>

<script>
// @ is an alias to /src
import ProductCard from '@/components/ProductCard.vue'

export default {
  name: 'HomeView',
  props: ['inventory', 'addToCart'],
  components: {
    ProductCard
  }
}
</script>
