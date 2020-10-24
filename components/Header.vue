<template>
  <header>
    <div class="container relative d-flex align-items-center py-3"> 
      <a href="/" class="top">ruru8.net</a>
      <b-nav class="w-100 d-flex justify-content-end font-weight-bold">
        <b-nav-item><nuxt-link to="/about">About</nuxt-link></b-nav-item>
        <b-nav-item><nuxt-link to="/blog">Blog</nuxt-link></b-nav-item>
      </b-nav>
    </div>
  </header>
</template>

<style lang="scss">
header {
  width: 100%;

  .top {
    font-size: 2.5em;
    &:hover {
      text-decoration: none;
    }
  }
}
</style>