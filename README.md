# carolines-vue-cheat-sheet

## Get started

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

Vue has a **views** directory to store the pages of the application which are connected to the router.

**components** are imported into the views or into each-other 

Here is how to import a component into a vue:

```vue
<template>
    <div class="home">
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