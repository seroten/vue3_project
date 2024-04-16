<template>
  <form @submit.prevent>
    <h4>Add a post</h4>
    <my-input
        v-model="post.title"
        type="text"
        placeholder="Name"/>
    <my-input
        v-model="post.body"
        type="text"
        placeholder="Description"/>
    <my-button class="btn" @click="addPost">Add</my-button>
  </form>
</template>
<script>

import MyInput from "@/components/UI/MyInput.vue";

export default {
  name: "PostForm",
  components: {MyInput},

  data() {
    return {
      post: {
        title: '',
        body: '',
      }
    }
  },
  methods: {
    addPost() {
      this.post.id = Date.now();
      this.$emit('createPost', this.post)
      this.post = {
        title: '',
        body: '',
      }
    }
  }
}
</script>

<style scoped>
form {
  display: flex;
  flex-direction: column;
}
.btn {
  align-self: flex-end;
}
</style>