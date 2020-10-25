<template>
  <header>
    <div class="container relative d-none d-sm-flex align-items-center py-3"> 
      <a href="/" class="top">ruru8.net</a>
      <b-nav class="w-100  justify-content-end font-weight-bold">
        <b-nav-item href="https://github.com/ruru8" target="_blank"><font-awesome-icon :icon="['fab', 'github']" /></b-nav-item>
        <b-nav-item href="https://twitter.com/_ruru8" target="_blank"><font-awesome-icon :icon="['fab', 'twitter']" /></b-nav-item>
        <b-nav-item><nuxt-link to="/about">About</nuxt-link></b-nav-item>
        <b-nav-item><nuxt-link to="/blog">Blog</nuxt-link></b-nav-item>
      </b-nav>
    </div>

    <div class="w-100 d-block d-sm-none">
      <b-navbar toggleable type="bright" variant="bright">
        <b-navbar-brand href="/" class="top">ruru8.net</b-navbar-brand>

        <b-navbar-toggle target="navbar-toggle-collapse" class="menu-trigger">
          <span></span>
          <span></span>
          <span></span>
        </b-navbar-toggle>

        <b-collapse id="navbar-toggle-collapse" is-nav>
          <b-navbar-nav class="ml-auto">
            <b-nav-item href="/about">About</b-nav-item>
            <b-nav-item href="/blog">Blog</b-nav-item>
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

  .top {
    font-size: 2.5em;
    font-weight: 200;
    &:hover {
      text-decoration: none;
    }
  }

  //  ハンバーガーメニュー
  .menu-trigger {
    position: relative;
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
}
</style>
