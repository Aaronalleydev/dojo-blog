<template>
  <div class="home">
    <h1>Home</h1>
    <PostList v-if="showPosts" :posts="posts"/>
    <button @click="showPosts = !showPosts">Toggle Posts</button>
    <button @click="posts.pop()">Delete a posts</button>
  </div>
</template>

<script>
import PostList from '../components/PostList.vue'
import { ref } from '@vue/reactivity'

// @ is an alias to /src

export default {
  name: 'Home',
  components: { PostList },
  setup() {
    
    const posts = ref([
      { title: 'Welcome to the blog', body: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec accumsan vel risus eget vulputate. Morbi gravida mauris sed odio aliquam vehicula. Etiam pretium, nisl interdum convallis ultrices, purus purus scelerisque dolor, a vehicula nunc ligula quis libero. Integer tempor nibh elementum convallis placerat. Phasellus fringilla et sem vel fringilla. Pellentesque quam erat, finibus eget nulla et, auctor consectetur mi. Nullam nec malesuada nibh, id faucibus turpis. Fusce eu aliquet urna. Mauris consequat et lacus a hendrerit. Aliquam justo lacus, dapibus at nisl vitae, porttitor iaculis tellus. Quisque sed aliquam elit, at porta nibh. \n Quisque lobortis facilisis risus condimentum vehicula. Etiam pellentesque non risus in dignissim. Donec ultricies hendrerit magna, in lobortis ex pretium ac. In accumsan porttitor rhoncus. Mauris porttitor elit et sem sodales vestibulum. Integer nisi ex, aliquet et accumsan congue, vehicula vel dolor. Pellentesque ullamcorper pharetra eros id tincidunt. Vivamus porttitor, dolor at volutpat laoreet, quam turpis dictum metus, sed aliquet ex tellus eget dolor. Mauris consectetur elit orci, consectetur cursus elit rhoncus nec. Praesent id placerat turpis, quis mollis magna. Vestibulum a lacinia nulla, in efficitur velit. Vestibulum suscipit posuere ligula, quis euismod lacus egestas a. Nunc id augue quis erat tincidunt pretium. Sed convallis risus vitae.', id: 1},
      { title: 'Top 5 CSS tips', body: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec accumsan vel risus eget vulputate. Morbi gravida mauris sed odio aliquam vehicula. Etiam pretium, nisl interdum convallis ultrices, purus purus scelerisque dolor, a vehicula nunc ligula quis libero. Integer tempor nibh elementum convallis placerat. Phasellus fringilla et sem vel fringilla. Pellentesque quam erat, finibus eget nulla et, auctor consectetur mi. Nullam nec malesuada nibh, id faucibus turpis. Fusce eu aliquet urna. Mauris consequat et lacus a hendrerit. Aliquam justo lacus, dapibus at nisl vitae, porttitor iaculis tellus. Quisque sed aliquam elit, at porta nibh. \n Quisque lobortis facilisis risus condimentum vehicula. Etiam pellentesque non risus in dignissim. Donec ultricies hendrerit magna, in lobortis ex pretium ac. In accumsan porttitor rhoncus. Mauris porttitor elit et sem sodales vestibulum. Integer nisi ex, aliquet et accumsan congue, vehicula vel dolor. Pellentesque ullamcorper pharetra eros id tincidunt. Vivamus porttitor, dolor at volutpat laoreet, quam turpis dictum metus, sed aliquet ex tellus eget dolor. Mauris consectetur elit orci, consectetur cursus elit rhoncus nec. Praesent id placerat turpis, quis mollis magna. Vestibulum a lacinia nulla, in efficitur velit. Vestibulum suscipit posuere ligula, quis euismod lacus egestas a. Nunc id augue quis erat tincidunt pretium. Sed convallis risus vitae. ', id: 2}
    ])

    const showPosts = ref(true)

    return { posts, showPosts }
  }
}
</script>
