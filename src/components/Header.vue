<template>
  <div class="Header">
    <div class="Header__image">
      <img alt="logo" src="https://orderingweb.ordering.co/templates/web/img/logo.png" />
    </div>
    <div class="Header__right_menu">
      <a href="#">Home</a>
      <a href="#">About</a>
      <a href="#">Login</a>
    </div>
  </div>
</template>

<style scoped>
.Header {
  height: 40px;
  display: flex;
  justify-content: space-between;
  border: 1px solid rgba(0, 0, 0, 0.3);
  border-radius: 10px;
}

.Header__image img {
  height: 100%;
}

.Header__right_menu {
  width: 300px;
  display: flex;
  justify-content: space-around;
  align-items: center;
}
</style>