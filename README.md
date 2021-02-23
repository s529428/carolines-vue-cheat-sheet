# carolines-vue-cheat-sheet

## Get started

**ONLY RUN VUE CREATE IF STARTING NEW PROJECT**
To start a new view project run the following command:

```Bash
vue create project-name
```

To do a multipe page app, pick the following settings
* Manually select features
    * Babel
    * Router
    * Vuex
    * CSS Pre-processors
    * Linter / Formatter
* Use history mode for router? Yes
* Sass/SCSS (with node-sass)
* ESLint + Standard config
* Lint on save
* In dedicated config files
* No
Hit enter and it wil install and generate needed files.

To get started and run the live preview run the following: 

```Bash
cd project-name
npm run serve
```

## The Basics

### Using components

Vue has a **views** directory to store the pages of the application which are connected to the router.

**components** are imported into the views or into each-other 

Here is how to import a component into a vue:

```vue
<template>
    <div class="home">
        <!-- The following element is how we display a component-->
        <HelloWord msg="Hello and welcome"/>
    </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
    name: 'home'
    components: {
        HelloWorld
    }
}
</script>
```

### Adding pages

In the `router.js` is how we hook up our pages. It will look like this:
```javascript
import Vue from 'vue'
import Router from 'vue-router'
import Home from './views/Home.vue'

Vue.use(Router)

export default new Router({
    mode: 'history',
    base: process.env.BASE_URL,
    routes: [
        {
            path: '/',
            name: 'home',
            component: Home
        },
        {
            //Additional pages would go here!
            //Follow a format simular to what is already here for the home page!
        },
    ]
})
```

In the `store.js` is where we create new stores which is a global object. Any function or variable or data would go into the `store.js` so that you can use it in multiple parts of the application.  

### Dynamic Routing

