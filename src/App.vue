<template>
<div id="nav">
  <ul>
    <li><h1>MyScratchPage</h1></li>
  </ul>
  </div>
  <input class="input-box" type="text" v-model="search" placeholder="User">
  <button onClick="fetchData()" id="queryBtn" class="btn">Go</button>
  <p class="status" type="text">{{status}}</p>
</template>

<script>
/* eslint-disable */
export default {
  name: 'App',
  components: {
  }
}

function fetchData() {
  return fetch('https://my-ocular.jeffalo.net/api/user/' + this.search)
    .then(response => response.json())
    .then(json => {
      this.status = json;
    });
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: white;
  background-color: #111;;
}
*{
  margin:0;
  padding:0;
}
body {
  top: 0;
  position: relative;
  background-color: #111;;
}
#nav {
  background-color: #222;
  list-style-type: none;
  padding: 3pt;
}
ul {
  list-style-type: none;
  display: flex;
}
.input-box {
  width: 90%;
  padding: 6pt;
  border: none;
  outline: none;
}
.btn {
  width: 10%;
  padding: 6pt;
  border: none;
  outline: none;
  background-color: #222;
  color: white;
}
</style>
