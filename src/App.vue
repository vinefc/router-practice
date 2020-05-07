<template>
  <div id="app">
  
    <router-view/>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  display: fex;
  flex-direction: column;
}

#nav {
  box-sizing: border-box;
  border: 10px;
  padding: 30px;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}

#nav a {
  
  box-sizing: border-box;
  border: solid;
  height: 50px;
  width: 50px;
  font-weight: bold;
  color: #0b6903;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>

