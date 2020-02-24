<template>
  <div id="app">
    <div id="title">
      <img id="logo" alt="Mark Tilton" src="./assets/MarkTilton.png" />
    </div>
    <div id="nav">
      <router-link class="routerlink" to="/">About</router-link>
      <router-link class="routerlink" to="/projects">Projects</router-link>
      <router-link class="routerlink" to="/contact">Contact</router-link>
      <router-link class="routerlink" to="/feeds">Feeds</router-link>
    </div>
    <router-view id="content" />
  </div>
</template>

<style>
@import "./styles/resources.css";

#app {
  margin: 20px;
  padding: 0px;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: var(--main-fg-color);
  position: relative;
  display: grid;
  grid-template-rows: auto auto;
  grid-template-columns: 100%;
}

#title {
  grid-row: 1/2;
  grid-column: 1/2;
  justify-self: left;
}

#logo {
  display: inline-block;
}

#name {
  display: inline-block;
}

#nav {
  padding: 10px;
  grid-row: 1/2;
  grid-column: 1/2;
  justify-self: right;
  height: fit-content;
  position: absolute;
  top: 50%;
  -ms-transform: translateY(-50%);
  transform: translateY(-50%);
  margin: 0;
  font-size: 18pt;
}

#nav a {
  font-weight: bold;
  color: var(--main-fg-color);
  text-decoration: none;
}

#nav a.router-link-exact-active {
  color: var(--main-hl-color);
}

#content {
  grid-row: 2 / 3;
}

.routerlink {
  margin: 0px 5px;
}
</style>
