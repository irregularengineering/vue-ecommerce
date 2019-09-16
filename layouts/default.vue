<template>
  <div>
    <nav class="navbar is-white has-shadow">
      <div class="container">
        <div class="navbar-brand">
          <router-link to="/" class="navbar-item is-size-3 logo has-text-dark">
            Wild<b>Bill</b> Hiccup's 
          </router-link>
        </div>
        <div class="navbar-menu is-active">
          <div class="navbar-end">
            <div class="navbar-item">
              <img src="../assets/cart.png">
              <nuxt-link :to="{name: 'cart'}"> Cart ({{ cartTotal }})</nuxt-link>
            </div>
          </div>
        </div>
      </div>
    </nav>
    <nuxt/>
    <footer class="footer">
      <div class="container">
        <div class="content has-text-centered">
          Proudly Powered By <a href="https://cosmicjs.com" class="has-text-dark"><strong>Cosmic JS</strong></a>
          <a href="https://cosmicjs.com/add-bucket?import_bucket=5d7feba607e621480c42770b"><img src="https://cdn.cosmicjs.com/51fe54d0-4f6e-11e9-9f32-8d001da69630-powered-by-cosmicjs.svg" /></a>
        </div>
      </div>
    </footer>
  </div>
</template>
<script>
  export default {
    computed: {
      cartTotal () {
        return this.$store.state.cartTotal
      }
    }
  }
</script>

<style>
body {
  background: #DAE2DB;
}
</style>
