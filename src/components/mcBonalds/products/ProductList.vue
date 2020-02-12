<template>
  <div class="container-fluid">
    <div
      class="productContainer row"
      v-for="(product, index) in products"
      :key="index"
    >
      <div class="productImage col-2">
        <img :src="product.images" alt="" />
      </div>
      <div class="productName col-5">
        {{ product.name }}
      </div>
      <div class="productButton col-5">
        <button class="btn btn-success">Add to cart</button>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'ProductList',
  props: {
    products: Array
  }
};
</script>

<style scoped>
.productContainer {
  margin: 5px 0;
  border-bottom: 1px solid rgba(0, 0, 0, 0.1);
}

.productImage,
.productName,
.productButton {
  display: flex;
  align-items: center;
  justify-content: center;
}

.productImage img {
  height: 50px;
}
</style>
