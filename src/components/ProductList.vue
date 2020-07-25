<template>
    <div>
        <div class="list-group bold">
          <div href="#" class="list-group-item list-group-item-action">
            <div class="row">
                <div class="col-md-4">Category</div>
                <div class="col-md-4">Product</div>
                <div class="col-md-4">Price</div>
            </div>
          </div>
        </div>

        <div class="list-group select" v-for="(product, index) in products" v-bind:key="index">
          <a class="list-group-item list-group-item-action">
            <!-- <router-link to="/product.index"> -->
            <router-link :to="`${index}/${product.category}/${product.name}/${product.price}`">
            <div class="row">
                <div class="col-md-4">{{ product.category }}</div>
                <div class="col-md-4">{{ product.name }}</div>
                <div class="col-md-4">{{ product.price }} $</div>
            </div>
            </router-link>
          </a>
        </div>
    </div>
</template>

<script>
import products from "../data/products";
export default {
  props: {
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
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {color: #2c3e50 !important;}

.btn-outline-success {color: #41b883 !important; border-color: #41b883;}
.btn-outline-success:hover {color: white !important; background-color: #41b883 !important; }

.bold {font-weight: 700}
.bold a, .bold a:hover {background-color: #41b8833d;}
.select a:hover {background-color: #41b8833d; text-decoration: none;}
</style>