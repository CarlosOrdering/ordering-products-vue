<template>
  <div id="app">
    <Header />
    <div class="container-fluid">
      <div class="row">
        <div class="col-8">
          <Store />
        </div>
        <div class="col-4">
          <Cart />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Store from './components/mcBonalds/Store.vue';
import Cart from './components/mcBonalds/Cart.vue';

export default {
  name: 'App',
  components: {
    Header,
    Store,
    Cart
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
