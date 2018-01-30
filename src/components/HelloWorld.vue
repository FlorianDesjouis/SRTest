<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>This is a single page application.</h2>
    <div>By clicking on <strong>Graphs</strong> in the menu you'll see a graphic using Streamroot<span style="font-size: 12px;">&copy;</span> datas</div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome on SR Graphs'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
}
</style>
