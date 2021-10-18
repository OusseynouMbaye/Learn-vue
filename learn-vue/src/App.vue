<template>
  <div>
    <h1 v-bind:title="sport">hello {{ name }}</h1>
    <div v-text="sport"></div>
    <div>allo <b v-html="series"> </b></div>
    <!-- binding attribute to use id -->
    <div>
      <h2 v-bind:id="headingId">Heading</h2>
      <!-- binding to use boolean -->
      <button v-bind:disabled="isDisabled">texte desactive</button>
    </div>
    <h2 class="underline">underline texte</h2>
    <div><h3 class="underline" v-bind:class="status">status</h3></div>
    <h3 v-bind:class="isEating && 'eating'" >eating dinner</h3>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      name: "Learn",
      sport: "Swimming",
      series: "NCIS",
      headingId: "heading",
      isDisabled: false,
      status: "success",
      isEating :true
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.underline {
  text-decoration: underline;
}
.eating{
  color: rgb(255, 72, 0);
}
</style>
