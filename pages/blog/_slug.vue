<template>
  <article>
    <b-container class="mt-2">
      <div class="date text-secondary">{{ moment(blog.date, "YYYY MMMM Do, dddd")}}</div>
      <h1>{{blog.title}}</h1>
      <!-- <div><img :src="blog.image" /></div> -->
      <div>
        <span v-for="tag in blog.tags" :key="tag" class="badge badge-info mr-2">{{tag}}</span>
      </div>
      <nuxt-content :document="blog" class="my-5"/>
    </b-container>
  </article>
</template>

<script lang="ts">
import { Vue, Component } from 'nuxt-property-decorator'
import { Context } from '@nuxt/types'
import moment from 'moment';

@Component
export default class Blog extends Vue{
  async asyncData({ $content, params, error }: Context) {
    const blog = await $content('blogs', params.slug).fetch()
    return { blog }
  }

  public moment(value: any, format: any) {
    return moment(value).format(format);
  }
}
</script>
<style lang="scss">
article{
  color: #2f495e;
}
.nuxt-content {
  
  h2 {
    margin: 1.6em 0px 0.8em 0px;
    padding-bottom: 5px;
    border-bottom: 1px solid #ddd;
  }

  h3 {
    margin: 1.6em 0px 0.8em 0px;
  }

  img {
    max-width: 100%;
  }

  a {
    word-break: break-all;
  }

  pre {
    background: whitesmoke;
  }
}
</style>