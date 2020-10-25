<template>
  <b-container class="blog">
    <h2 class="mb-4">Blog</h2>
    <div v-for="blog in blogs" :key="blog.slug">
      <div class="mb-3">
        <div class="date text-secondary">
          <small>{{ moment(blog.date, "YYYY MMMM Do, dddd")}}</small>
        </div>
        <div class="link">
          <nuxt-link :to="'/blog/'+ blog.slug">{{blog.title}}</nuxt-link>
        </div>
      </div>
    </div>
  </b-container>
</template>

<script lang="ts">
import { Vue, Component } from 'nuxt-property-decorator'
import { Context } from '@nuxt/types'
import moment from 'moment';


@Component
export default class Blog extends Vue{
  async asyncData({ $content, params, error }: Context) {
    const blogs = await $content('blogs').sortBy('date', 'desc').fetch()
    return { blogs }
  }

  public moment(value: any, format: any) {
    return moment(value).format(format);
  }
}
</script>

<style>

</style>