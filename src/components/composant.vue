<template>
  <h1>allo</h1>
  <h3>{{ texte }}</h3>
  <h4>{{ chiffre }}</h4>
  <button v-on:click="chiffre++"> + </button>
</template>

<script>
export default {
    props: {
        texte : String
    },
    data() {
        return {
            chiffre : 0
        }
    }
}
</script>

<style>
 h1 {
     color: blue;
 }
</style>

-------------------------

<Composant :texte="bonsoir"/>