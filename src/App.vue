<template>
  <div id="app">
    <!-- <div id="nav">
      <router-link to="/">خانه</router-link> |
      <router-link to="/about">درباره</router-link>
    </div>-->

    <nav class="navbar is-light" role="navigation" aria-label="main navigation">
      <div class="navbar-brand">
        <router-link class="navbar-item except" to="/">
          <img src="./assets/logo.png" alt="Website logo" />
        </router-link>
        <a
          role="button"
          class="navbar-burger burger"
          aria-label="menu"
          aria-expanded="false"
          data-target="navMenu"
          v-bind:class="isActive ? 'is-active' : ''"
          v-on:click="isActive = !isActive"
        >
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
        </a>
      </div>

      <div id="navMenu" class="navbar-menu" v-bind:class="isActive ? 'is-active' : ''">
        <div class="navbar-start">
          <router-link class="navbar-item has-text-primary" to="/">صفحه اصلی</router-link>
          <router-link class="navbar-item" to="/avout">درباره من</router-link>
        </div>
      </div>
    </nav>

    <router-view />
  </div>
</template>

<script>
export default {
  data() {
    return {
      isActive: false
    };
  }
};
</script>

<style lang="scss">
@import "assets/style/index.css";
body {
  direction: rtl;
}
</style>
