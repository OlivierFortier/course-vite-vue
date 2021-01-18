<template>
  <article>
    <p v-for="comment in commentaires" :key="comment">{{ comment.body }}</p>
  </article>
</template>

<script>
export default {
  props: {
    texteMaximum: Number,
  },
  data() {
    return {
      commentaires: null,
    };
  },
  beforeCreate() {
    fetch("https://jsonplaceholder.typicode.com/posts")
      .then((reponse) => reponse.json())
      .then((resultat) => {
        const tableauFiltrer = resultat.slice(0, this.texteMaximum);

        this.commentaires = tableauFiltrer;
      });
  },
};
</script>

<style>
article {
  border: 1px solid black;
}
</style>
