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
    <h3 v-bind:class="isEating && 'eating'">eating dinner</h3>
    <!-- bind style with object methode -->

    <h2 v-bind:style="styleObject">methode to bind with object</h2>
    <!-- bind style with array methode -->
    <div>
      <h2 :style="[baseStyleObject, successStyleObject]">
        methode to bind with array 1
      </h2>
      <h2 :style="[baseStyleObject, dangerStyleObject]">
        methode to bind with array 1
      </h2>
      <h2 v-if="num === 0">the numer is zero</h2>
      <h3 v-if="num < 0">the number is negative</h3>
      <h3 v-if="num > 0">the number is positive</h3>
      <h3 v-else>Not a number</h3>
    </div>
    <template v-if="display">
      <h2>v-if</h2>
      <h3>v-else</h3>
      <h4>vue</h4>
    </template>
    <div>
      <h4 v-show="sunday">this is v-show</h4>
      <h4 v-if="sunday">this is v-show hidden</h4>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      sunday: false,
      num: "allo",
      display: true,
      name: "Learn",
      sport: "Swimming",
      series: "NCIS",
      headingId: "heading",
      isDisabled: false,
      status: "success",
      isEating: true,
      styleObject: {
        color: "blue",
        fontSize: "34px",
        // float: "right",
      },
      baseStyleObject: {
        fontSize: "50px",
        padding: "10px",
      },
      successStyleObject: {
        color: "green",
        backgroundColor: "lightgreen",
        border: "1px solid green",
      },
      dangerStyleObject: {
        color: "red",
        backgroundColor: "darkred",
        border: "1px solid red",
      },
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
.eating {
  color: rgb(255, 72, 0);
}
</style>
