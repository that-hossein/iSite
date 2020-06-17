<template>
  <div id="app">
    <nav
      class="navbar is-white is-fixed-top has-shadow"
      role="navigation"
      aria-label="main navigation"
    >
      <div class="navbar-brand">
        <router-link class="navbar-item" to="/">
          <img src="./assets/logo.png" alt="Website logo" />
        </router-link>
        <a
          role="button"
          class="navbar-burger burger"
          aria-label="menu"
          aria-expanded="false"
          data-target="navMenu"
          v-bind:class="navShown ? 'is-active' : ''"
          v-on:click="navShown = !navShown"
        >
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
        </a>
      </div>

      <div id="navMenu" class="navbar-menu" v-bind:class="navShown ? 'is-active' : ''">
        <div class="navbar-end">
          <router-link class="navbar-item" to="/" @click.native="navShown = false">صفحه اصلی</router-link>
          <router-link class="navbar-item" to="/about" @click.native="navShown = false">درباره من</router-link>
        </div>
      </div>
    </nav>

    <keep-alive>
      <router-view />
    </keep-alive>
  </div>
</template>

<script>
export default {
  data() {
    return {
      navShown: false
    };
  },
  methods: {
    addtohtml() {
      const el = document.body;
      el.classList.add("has-navbar-fixed-top");
    }
  },
  mounted() {
    this.addtohtml();
  }
};
</script>

<style lang="scss">
@import "assets/style/index.css";
@import "assets/style/my-bulma/sass/mybulma.scss";
body {
  direction: rtl;
}
.router-link-exact-active {
  color: $primary !important;
}
.navbar-burger {
  margin-right: auto !important;
  margin-left: 0 !important;
}
</style>
