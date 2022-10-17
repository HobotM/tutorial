
<template>
  <section>
    <p v-if="likes > 0">
      this presentation has {{ likes }} likes
    </p>

    <p v-else>
      nobody likes it

    </p>
    <button v-on:click="presentation()">
      Like
    </button>
  </section>

</template>

<script>
import Vue from 'vue'
export default {

  data () {
    return {
      likes: 0
    }
  },
  methods: {
    presentation () {
      this.likes++
    }
  }

}

</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}

button {
  display: inline-block;
  padding: 0.35em 1.2em;
  border: 0.1em solid #FFFFFF;
  margin: 0 0.3em 0.3em 0;
  border-radius: 0.12em;
  box-sizing: border-box;
  text-decoration: none;
  font-family: 'Roboto', sans-serif;
  font-weight: 300;
  color: white;
  text-align: center;
  transition: all 0.2s;
  background-color: blue;
}

button:hover {
  color: white;
  background-color: black;
}

@media all and (max-width:30em) {
  button {
    display: block;
    margin: 0.4em auto;
  }
}
</style>
