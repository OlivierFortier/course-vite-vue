<template>
  <h1>Un exemple d'application vue.js pour donner un cours d'introduction</h1>
  <main>
    <MonArticle :texteMaximum="2"/>
    <MonArticle :texteMaximum="4"/>
    <MonAside/>
    <MonAside/>
    <MonAside/>
    <MonAside/>
  </main>
</template>

<script>
import MonArticle from "./components/MonArticle.vue";
import MonAside from "./components/MonAside.vue";

export default {

  components : {
    MonArticle,
    MonAside,
  }

};
</script>

<style>
body {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 80%;
  margin: 0 auto;
}
</style>
