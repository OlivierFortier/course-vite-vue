<template>
  <article>
    <p v-for="comment in commentaires" :key="comment">{{ comment.body }}</p>
  </article>
</template>

<script>
export default {
  data() {
    return {
      commentaires: null,
    };
  },
  beforeCreate() {

    fetch("https://jsonplaceholder.typicode.com/posts")
      .then(reponse => reponse.json())
      .then(blessure => this.commentaires = blessure);

  },

};
</script>

<style>
article {
  border: 1px solid black;
}
</style>
