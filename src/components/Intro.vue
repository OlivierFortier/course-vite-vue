<template>
  <div>
    <p>allo</p>
    <h1 class="fond-noir" id="yeet">bonsoir</h1>
    <span> {{ allo }} </span>
    <span> {{ compteur }}</span>
  </div>
</template>

<style scoped>
.fond-noir {
  background-color: slategray;
  color: whitesmoke;
}
</style>

<script>
export default {
  data() {
    return {
      allo: "coucou",
      compteur: 0,
    };
  },
};
</script>
