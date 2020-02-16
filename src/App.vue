<template>
  <div id="app">
    <img id="logo" alt="Vue logo" src="./assets/logo.png">
    <div id="nav">
      <router-link to="/">About Me</router-link> |
      <router-link to="/about">Projects</router-link> |
      <router-link to="/about">Contact</router-link> |
      <router-link to="/about">Feeds</router-link>
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
  grid-row: 1 / 2;
  grid-column: 1/2;
  justify-self: right;
  height: fit-content;
  position:absolute;
  top: 50%;
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
