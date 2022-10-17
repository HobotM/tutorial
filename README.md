# tutorial

## Project setup

### Use the following command to install the Vue.Js globally on your machine.
```
npm install -g @vue/cli
```

### To create a new project use a create 'project name' command and cd to your project folder
```
vue create vue-starter-project
cd vue-starter-project
```

### To build and run a project use 
```
npm run serve
```

### Import Vue from vue
### export default is used to create local registration for Vue component
### data is a function that returns the initial reactive state for the component instance. The function is expected to return a plain JavaScript object, which will be  made reactive by Vue. It will be created 
```
import Vue from 'vue'
export default {
  data () {
    return {
      likes: 0,
      dislikes: 0
    }
  },
```



### Inside the template section create p tags use v-if and v-else directives to output the data on the screen.
### v-on button listens to the DOM events and allows to manipulate the data, with a method that we can call from a methods secion inside the script tag.
### Create the equvalent code for dislike option.
```
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
```

### methods is a section that we can call from the HTML section, and it triggers the changes in the data depends on the action on the screen.
### presentation() method for likes and no() method for dislikes data, both are set up to increment by 1.
```
// 
  methods: {
    presentation () {
      this.likes++
    // presentation method to increment likes by one
    },
    no () {
      this.dislikes++
      // no method to increment dislikes by one
    }
```
### Additional styling using scss, mainly for button and position of out data on the screen
```
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
