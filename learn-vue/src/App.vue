<template>
<h1> hello {{name}}</h1>
<div v-text="sport"></div>
</template>

<script>


export default {
  name: 'App',
  data(){
    return {
      name : "Learn",
      sport : 'Swimming',
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
</style>
