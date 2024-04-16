<template>
<div>
  <h3>Список постов</h3>
  <post-item
      v-for="post in posts"
      :post="post"
  />
</div>
</template>

<script>
import PostItem from "@/components/PostItem.vue";

export default {
  components: {PostItem},
  // name: "PostList",
  props: {
    posts: {
      type: Array,
      required: true
    }
  },
  data() {
    return {

    }
  }
}
</script>

<style scoped>

</style>