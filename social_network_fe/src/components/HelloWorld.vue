<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      For a guide and recipes on how to configure / customize this project,<br>
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>
    <h3>Installed CLI Plugins</h3>
    <post v-for="post in posts" :key="post.slug" :text="post.content.text" :user="post.user" />
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import Post from './Post.vue';

export default Vue.extend({
  name: 'HelloWorld',
  components: {
    Post,
  },
  props: {
    msg: String,
  },
  data() {
    return {
      posts: [
        {
          slug: 'shavs-text-01',
          user: 'Shavs',
          type: 'text',
          content: {
            text: 'I just posted some text to this Social Media',
          },
        },
        {
          slug: 'yorch-video-01',
          user: 'Yorch',
          type: 'media/video',
          content: {
            text: 'Check this out! You can stream video using Amazon S3 and Nest JS',
          },
        },
        {
          slug: 'batsy-photo-01',
          user: 'Batsy',
          type: 'media/photo',
          content: {
            text: 'This photos are stored inside a Flickr bucket. Awesome!',
          },
        },
      ],
    };
  },
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
