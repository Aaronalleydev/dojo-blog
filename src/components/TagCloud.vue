<template>
  <div class="tag-cloud">
    <h3>Tags</h3>
    <div v-for="tag in tags" :key="tag" class="tagLinks">
      <router-link :to="{ name: 'Tag', params: { tag: tag}}">
        #{{ tag }}
      </router-link>
    </div>
    <div>

    </div>
  </div>
</template>

<script>

import useTags from '../composoables/useTags'
export default {
  props: ['posts'],
  setup(props) {
    const { tags } = useTags(props.posts)

    return { tags }
  }
}
</script>

<style>
  .tagLinks a {
    text-decoration: none;
    color: grey;
    cursor: pointer;
  }
 .tagLinks {
   display: inline-block;
   margin-left: 10px;
 }
</style>