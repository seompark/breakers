<template>
  <nav :class="{
    navbar: true,
    'navbar--white': black
  }">
    <div class="navbar__brand">
      <img
        :src="computedLogo"
        @click="goHome"
        class="navbar__logo">
    </div>
    <div class="navbar__menu">
      <router-link :class="computedMenuItemClass" to="/funding">Funding</router-link>
      <router-link :class="computedMenuItemClass" to="/shop">Shop</router-link>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'VNavbar',
  props: {
    black: Boolean,
    white: Boolean
  },

  methods: {
    goHome () {
      this.$router.push('/')
    }
  },

  computed: {
    computedLogo () {
      if (this.black) return require('@/assets/images/logo-black.png')
      if (this.white) return require('@/assets/images/logo-white.png')
      return require('@/assets/images/logo-colored.png')
    },
    computedMenuItemClass () {
      return {
        'navbar__menu-item': true,
        'navbar__menu-item--white': this.white
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.navbar {
  display: flex;
  align-items: center;
  background-color: transparent;
  padding: 25px 60px;
}

.navbar--white {
  background-color: #fff;
}

.navbar__logo {
  cursor: pointer;
  height: 50px;
}

.navbar__menu {
  display: flex;
  margin-left: auto;
}

.navbar__menu-item {
  font-family: "SF Display", sans-serif;
  margin-left: 70px;
  font-size: 18px;
  cursor: pointer;
  text-decoration: none;
  color: #000;
  &--white {
    color: #fff;
  }
  :visited {
    color: #000;
  }
}

</style>
