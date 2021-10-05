<template>
    <div class="post" v-for="post in posts">
      <div><strong>Пост о </strong> {{ post.title }}</div>
      <div>{{ post.body }}</div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
.post {
  border: 3px solid green;
  border-radius: 0;
  width: 50%;
  margin-top: 3%;
  margin-left: 2%;
}
</style>