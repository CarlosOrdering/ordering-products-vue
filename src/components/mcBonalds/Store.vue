<template>
  <div>
    <div
      class="categories card m-2"
      v-for="(categorie, index) in this.categories"
      v-bind:key="index"
    >
      <div class="title">
        <h3>{{ categorie.name }}</h3>
      </div>
      <ProductList v-bind:products="categorie.products" />
    </div>
  </div>
</template>
<script>
import axios from 'axios';
import ProductList from './products/ProductList.vue';

export default {
  name: 'Store',
  components: {
    ProductList
  },
  data: function() {
    return {
      categories: {}
    };
  },
  methods: {
    async fetchData() {
      const categories = await axios.get(
        'https://apiv4.ordering.co/v400/en/demo/business/41/categories'
      );
      this.categories = categories.data.result;
    }
  },
  beforeMount() {
    this.fetchData();
  }
};
</script>

<style scoped>
.title {
  margin: 30px;
  border-bottom: 1px solid rgba(0, 0, 0, 0.2);
}
</style>
