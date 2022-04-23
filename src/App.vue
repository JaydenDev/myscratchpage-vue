
<template>
<div id="nav">
  <ul>
    <li><h1>MyScratchPage</h1></li>
  </ul>
  </div>
  <input class="input-box" type="text" v-model="search" placeholder="User">
</template>

<script>
export default {
  name: 'App',
  components: {
  }
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
  width: 100%;
  padding: 6pt;
  border: none;
  outline: none;
}
</style>
