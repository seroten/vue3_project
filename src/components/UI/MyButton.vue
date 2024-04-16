<template>
  <button>
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: "MyButton"
}
</script>

<style scoped>
button {
  margin-top: 15px;
  padding: 10px 30px;
  background: none;
  color: teal;
  border: 1px solid teal;
}
</style>