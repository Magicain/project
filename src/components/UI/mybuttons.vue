<template>
  <button class="btn">
      <slot></slot>
  </button>
</template>

<script>
export default {
  name: 'mybutton'
}
</script>

<style scoped>
.btn {
    background: #fff;
    border: 1px solid #89c400;
    padding: 1em 3em;
    margin: 1em 0;
    align-self: flex-end;
}
</style>