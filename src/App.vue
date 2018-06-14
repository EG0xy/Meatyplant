<template>
  <div id="app">
    <header></header>
    <div class="content"></div>
    <footer>
          <nav class="main-nav">
            <ul>
                <router-link tag="li" to="/home" exact>Home</router-link>
                <router-link tag="li" to="/search">Search</router-link>
                <router-link tag="li" to="/cart">Cart</router-link>
                <router-link tag="li" to="/mine">Mine</router-link>
            </ul>
        </nav> 
       </footer>
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
