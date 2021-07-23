<template>
  <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About Me</router-link>
  </div>
  <router-view/>
</template>

<style>
* {
  font-family: courier;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  font-size: 1.1em;
  color: #000;
  text-decoration: none;
  padding: 0 10px;
}

#nav a:hover {
  opacity: 0.8;
}

#nav a.router-link-exact-active {
  color: #de1b31;
}
</style>
