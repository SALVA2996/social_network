<template>
  <div class="post">
    <span>{{ user }}</span> - {{ text }}
  </div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'HelloWorld',
  props: {
    user: String,
    text: String,
  },
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  .post {
    color: 'red';

    > span {
      font-weight: bold;
    }
  }
</style>
