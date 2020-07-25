<template>
  <div>
    <div class="hello">
      <h1>Welcome to The Vue.js App</h1>
    </div>
    <button @click="toggler" class="btn btn-outline-success btn-lg mt-3">Take a look at our shop</button>
    <div v-if="toggle" class="text-center container">
        <ProductList class="mt-4"/>
    </div>
  </div>
</template>

<script>
import products from "../data/products";
import ProductList from './ProductList'
export default {
  props: {
  },
  components: {
    ProductList
  },
  data () {
    return {
      toggle: false,
      products
    }
  },
  methods: {
    toggler() {
      this.toggle = !this.toggle
    }
  }
}
</script>

<style>
.container {max-width: 50%;}

a {color: #42b983;}

.btn-outline-success {
  color: #35495e !important;
  border-color: #35495e;
  }
.btn-outline-success:hover {
  color: white !important;
  background-color: #35495e !important;
  border-color: #35495e;
  }
</style>
