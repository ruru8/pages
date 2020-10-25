<template>
  <header>
    <div class="pc-nav container relative d-none d-sm-flex align-items-center py-2"> 
      <nuxt-link to="/" class="top-logo">ruru8.net</nuxt-link>
      <b-nav class="w-100  justify-content-end font-weight-bold">
        <b-nav-item href="https://github.com/ruru8" target="_blank"><font-awesome-icon :icon="['fab', 'github']" /></b-nav-item>
        <b-nav-item href="https://twitter.com/_ruru8" target="_blank"><font-awesome-icon :icon="['fab', 'twitter']" /></b-nav-item>
        <b-nav-item><nuxt-link to="/about">About</nuxt-link></b-nav-item>
        <b-nav-item><nuxt-link to="/blog">Blog</nuxt-link></b-nav-item>
      </b-nav>
    </div>

    <div class="sp-nav d-block d-sm-none">
      <b-navbar-toggle target="navbar-toggle-collapse" class="menu-trigger">
        <span></span>
        <span></span>
        <span></span>
      </b-navbar-toggle>
      <b-navbar toggleable type="bright" variant="bright" class="p-0">
        <b-navbar-brand class="pl-3"><nuxt-link to="/" class="top-logo">ruru8.net</nuxt-link></b-navbar-brand>

        <b-collapse id="navbar-toggle-collapse" is-nav>
          <b-navbar-nav class="ml-auto pl-3 pt-4 pb-3">
            <b-nav-item><nuxt-link to="/">Top</nuxt-link></b-nav-item>
            <b-nav-item><nuxt-link to="/about">About</nuxt-link></b-nav-item>
            <b-nav-item><nuxt-link to="/blog">Blog</nuxt-link></b-nav-item>
            <div class="py-2">
              <a href="https://github.com/ruru8" target="_blank" class="mr-2"><font-awesome-icon :icon="['fab', 'github']" /></a>
              <a href="https://twitter.com/_ruru8" target="_blank" class="mr-2"><font-awesome-icon :icon="['fab', 'twitter']" /></a>
            </div>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </div>

  </header>
</template>

<style lang="scss">
header {
  width: 100%;
  background-color: white;

  .top-logo {
    font-size: 2.5em;
    font-weight: 200;
    &:hover {
      text-decoration: none;
    }
  }

  .sp-nav {
    //  ハンバーガーメニュー
    .menu-trigger {
      position: fixed;
      top: 20px;
      right: 15px;
      z-index: 10;
      width: 32px;
      height: 30px;
      
      span {
        display: inline-block;
        transition: all .4s;
        position: absolute;
        left: 0;
        width: 100%;
        height: 3px;
        background-color: darkgray;
        border-radius: 4px;

        &:nth-of-type(1) {
          top: 0;
        }
        &:nth-of-type(2) {
          top: 13px;
        }
        &:nth-of-type(3) {
          bottom: 0;
        }
      }

      &.not-collapsed {
        span {
          &:nth-of-type(1) {
            -webkit-transform: translateY(12px) rotate(-45deg);
            transform: translateY(12px) rotate(-45deg);
          }
          &:nth-of-type(2) {
            opacity: 0;
          }
          &:nth-of-type(3) {
            -webkit-transform: translateY(-12px) rotate(45deg);
            transform: translateY(-12px) rotate(45deg);
          }
        }
      }
    }
    .navbar-collapse {
      position: fixed;
      top: 0;
      background: white;
      width: 100%;
      z-index: 9;
      border-bottom: 1px solid #ddd;
    }
  }
}
</style>
