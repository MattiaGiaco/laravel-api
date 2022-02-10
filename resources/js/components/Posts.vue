<template>
  <main class="container">
    <h3>I miei Posts</h3>
    <PostItem />
    <PostItem />
    <PostItem />
  </main>
</template>

<script>
import PostItem from './partials/PostItem.vue';

export default {
  name: 'Posts',
  components: {
    PostItem
  },
  data(){
    return{
      apiUrl: 'http://127.0.0.1:8000/api/posts'
    }
  },
  mounted(){
    this.getPosts();
  },
  methods: {
    getPosts(){
      axios.get(this.apiUrl)
            .then(res => {
              console.log(res.data)
            })
    }
  }
}
</script>

<style lang="scss" scoped>
  main{
    padding: 50px 0;
    h3{
      margin-bottom: 30px;
    }
  }
</style>