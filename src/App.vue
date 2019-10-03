<template>
  <div id="app">
    
    <HelloWorld v-for="dan in dana" v-bind:key="dan" :msg="dan"/>

  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld";

export default {
  name: "App",
   data() {
    return {
     dana: ["aa","bb","cc","dd","ff","gg","zz","oo","üü"],
     mal: "aa"
    }},
  components: {
    HelloWorld
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background-color: gray;
  margin-top: 60px;
  display: flex;
  flex-wrap: wrap;
  width: 320px;
  justify-content: center;
}
</style>
