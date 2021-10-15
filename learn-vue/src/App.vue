<template>
<h1 v-bind:title="sport"> hello {{name}}</h1>
<div v-text="sport"></div>
<div> allo <b v-html="series"> </b></div>
<!-- binding attribute to use id -->
<h2 v-bind:id="headingId"> Heading</h2>
<!-- binding to use boolean -->
<button v-bind:disabled="isDisabled">texte desactive</button>
<h2 class="underline"> underline texte</h2>
<h3 v-bind:class="status">ok</h3>
</template>

<script>


export default {
  name: 'App',
  data(){
    return {
      name : "Learn",
      sport : 'Swimming',
      series : "NCIS",
      headingId : "heading",
      isDisabled : false,
      status : "danger",
    }
  }
}
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
.underline{
  text-decoration: underline;
}
</style>
