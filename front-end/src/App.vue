<template>
  <div id="app">
    <div id="nav">
      <h1>AmericanJeremy Folklore Project</h1>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/>
    <div class="footer">
    <a href="https://github.com/jeremymlewis/folklore2">GitHub Repo</a>
  </div>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background-image: url('images/forest.jpg');
  color: #2c3e50;
}

#nav {
  padding: 30px;
  background-color: lightgray
}

.footer {
  height: 50px;
  padding: 20px 100px 0px 100px;
  background: #e3e3e3;
  font-size: 12px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
