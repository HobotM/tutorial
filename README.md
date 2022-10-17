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
### data is a function that returns the initial reactive state for the component instance. The function is expected to return a plain JavaScript object, which will be ### made reactive by Vue. It will be created 
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



### html
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

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
