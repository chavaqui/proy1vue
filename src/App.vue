
import router from './router';

<template>
  <nav>
    <router-link to="/" class="top-bar-link">
      <i class="iconfont-spoon-and-fork"></i>
      <span> Home</span>
    </router-link> |
    <router-link to="products" class="top-bar-link">
      <span>Products</span>
    </router-link> |
    <router-link to="past-orders" class="top-bar-link">
      <span>Past Orders</span>
    </router-link> |
     <router-link to="/about">About</router-link> |
     <router-link to="/MostrarExView">MostrarExcel</router-link>
  </nav>
  <router-view/>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
