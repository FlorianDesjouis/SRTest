<template>
  <main id="app">
    <nav>
      <ul class="menu">
        <li><router-link to="/">Home</router-link></li>
        <li><router-link to="/graphs">Graphs</router-link></li>
      </ul>
    </nav>
    <router-view></router-view>
  </main>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
  body {
    margin: 0;
  }
  .sayHello{
    margin-top: 10px;
  }
  .menu{
    color: #ffffff;
  }
  nav{
    width: 100%;
    height: 50px;
    display: flex;
    top: 0;
    background-color: #696969;
  }
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
  }

  h1, h2 {
    font-weight: normal;
  }

  ul {
    list-style-type: none;
    padding: 0;
  }

  li {
    display: inline-block;
    margin: 0 10px;
  }

  a {
    color: #42b983;
    cursor: pointer;
  }
  a:hover {
    color: #A2C0A2;
  }
</style>
