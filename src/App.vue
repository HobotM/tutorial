
<template>
  <section>
    <!-- Section with paragraphs and button to show an like data output on the page using v-if and v-else -->
    <p v-if="likes > 0">
      this presentation has {{ likes }} &#128077;
    </p>

    <p v-else>
      Who likes it?
    </p>
<!-- v-on click triggeres an event handler that changes the data which is displayed on the screen -->
    <button v-on:click="presentation()">
      Like
    </button>
  </section>

  <!-- Section with paragraphs and button to show an dislike data output on the page using v-if and v-else -->
  <section>
    <p v-if="dislikes > 0">
      this presentation has {{ dislikes }} &#128078;
    </p>

    <p v-else>
     Who dislikes it?
    </p>
<!-- v-on click triggeres an event handler that changes the data which is displayed on the screen -->
    <button v-on:click="no()">
      Dislike
    </button>
  </section>

</template>

<script>
import Vue from 'vue'
export default {
// JavaScript expression with props likes and dislikes with values set to 0 to began with
  data () {
    return {
      likes: 0,
      dislikes: 0
    }
  },
  // methods is a section that we can call from the HTML section, and it triggers the changes in the data depends on the action on the screen.
  methods: {
    presentation () {
      this.likes++
    // presentation method to increment likes by one
    },
    no () {
      this.dislikes++
      // no method to increment dislikes by one
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
