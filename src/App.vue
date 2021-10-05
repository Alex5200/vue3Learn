<template>
  <post-form />
  <postlist />
</template>

<script>
import PostForm from './components/postform.vue'
import Postlist from './components/postlist.vue'
export default {
  components: {
    PostForm, Postlist
  },
  data() {
    return {
      posts: [
        { id: 1, title: "Javascript", body: "Описание" },
        { id: 2, title: "Vue", body: "Описание" },
        { id: 3, title: "React", body: "Описание" },
      ],
      title: "",
      body: "",
    };
  }, 
  methods: {
    createPost(){
        const newPost = {
            id: Date.now(),
            title: this.title,
            body: this.body
        }
        this.posts.push(newPost)
        this.title = this.body = '';
    },
    
  },
};
</script>

<style >

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

</style>