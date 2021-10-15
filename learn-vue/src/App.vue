<template>
  <h1>hello {{ name }}</h1>
  <div v-text="sport"></div>
  <div v-html="serie"></div>
  <p>En utilisant la directive `v-html` : <span v-html="rawHtml"></span></p>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      name: "Learn",
      sport: "Swimming",
      serie: "<b>Chicago Med</b>",
      rawHtml:"testttt",
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
</style>
