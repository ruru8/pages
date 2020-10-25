<template>
  <b-container class="about">
    <h2 class="mb-4">About</h2>
    <div>
      <div class="py-3">
        <div class="topic"><font-awesome-icon :icon="['fas', 'user']"></font-awesome-icon> Name</div>
        <div class="ml-3">ruru8 / Chiharu Yasuda</div>
      </div>
      <div class="py-3">
        <div class="topic"><font-awesome-icon :icon="['fas', 'birthday-cake']"></font-awesome-icon> Birthday</div>
        <div class="ml-3">1997.01.19</div>
      </div>
      <div class="py-3">
        <div class="topic"><font-awesome-icon :icon="['fas', 'home']"></font-awesome-icon> From</div>
        <div class="ml-3">Saitama Kawaguchi</div>
        <div class="ml-3">今は都内在住です</div>
      </div>
      <div class="py-3">
        <div class="topic"><font-awesome-icon :icon="['fas', 'pencil-alt']"></font-awesome-icon> Skill</div>
        <div class="ml-3">業務で使ったもの</div>
        <div class="ml-3">Rails / Sinatra / Angular / Bootstrap / AWS / GAS / nginx / fluent-bit</div>
        <div class="ml-3">趣味や触ったことある程度のもの</div>
        <div class="ml-3">Vue / Nuxt.js / Python</div>
      </div>
      <div class="py-3">
        <div class="topic"><font-awesome-icon :icon="['fas', 'heart']"></font-awesome-icon> Like</div>
        <div class="ml-3">邦楽ロックを聞いたり、フェスやライブに行くこと。</div>
        <div class="ml-3">大学のサークルで始めたブレイクダンスを今でもちょくちょくやっています。</div>
      </div>
    </div>
  </b-container>
</template>

<style lang="scss">
.topic {
  font-weight: 600;
}
</style>