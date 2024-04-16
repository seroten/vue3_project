<template>
  <div class="app">
    <post-form
        @createPost="createPost"
    />
    <post-list
        :posts="posts"
    />
  </div>

</template>

<script>
import PostForm from "@/components/PostForm.vue";
import PostList from "@/components/PostList.vue";

export default {
  components: {PostList, PostForm},
  data() {
    return {
      posts: [
        {id: 1, title: 'Post about JS', body: 'Description'},
        {id: 2, title: 'Post about Java', body: 'Description2'},
        {id: 3, title: 'Post about NodeJS', body: 'Description3'},
        {id: 4, title: 'Post about NodeJS', body: 'Description4'}
      ],
    }
  },
  methods: {
    createPost(post) {
      this.posts.push(post);
    }
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.app {
  padding: 20px;
}
</style>