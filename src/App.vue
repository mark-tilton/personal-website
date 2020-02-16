<template>
  <div id="app">
    <img id="logo" alt="Vue logo" src="./assets/logo.png">
    <div id="nav">
      <router-link to="/">About</router-link> |
      <router-link to="/projects">Projects</router-link> |
      <router-link to="/contact">Contact</router-link> |
      <router-link to="/feeds">Feeds</router-link>
    </div>
    <router-view id="content" />
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  position: relative;
  display: grid;
  grid-template-rows: auto auto;
  grid-template-columns: 100%;
}

#logo {
  grid-row: 1/2;
  grid-column: 1/2;
  width:128px;
  height:128px;
}

#nav {
  padding: 10px;
  grid-row: 1 / 2;
  grid-column: 1/2;
  justify-self: right;
  height: fit-content;
  position:absolute;
  top: 50%;
  -ms-transform: translateY(-50%);
  transform: translateY(-50%);
  margin: 0;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

#content {
  grid-row: 2 / 3;
}

</style>
