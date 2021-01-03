# NOTE.md

This is some nodes when I learning vue

# Start a new vue project
* reference
  * [beginner-vuejs-tutorial-with-user-login](https://auth0.com/blog/beginner-vuejs-tutorial-with-user-login/)

1. use npm to install vue cli
```
npm install -g @vue/cli
```
2. use vue cli to create a new vue project
```
vue create <project_name>
```
3. I choice the typescript, vue2 and router

# Basic Structrue

## index.html
* entry point of browser
* where the "app" object is

## main.ts 
1. entry point of vue project.
2. create vue instance here, this instance mount on the #app object on DOM, which you can find in index.html

## App.vue
1. it was importing and rendering a template called App in main.ts

# vue

## data()
1. the following is smilar
```
data(){
  return {
    counter: 0
  }
}
```

```
data: function() {
  return {
    counter: 0
  }
}
```

if you use the following code, which may cause every single instance of this component share this property
```
data: {
  counter
}
```
2. data() will return the data which you want to use in template. gererally, you will get the data from API or some other ways.

# v-bind 
1. In Vue, ":" is shorthand for v-bind
2. v-bind can assign the value to become the property value of the component.
3. you can add a property by add the props:[] 

# v-for
1. is a for loop to generate component
```
v-for="element in list"
or 
v-for="(element, index) in list"
```
2. you can bind the unique key to each element by useing :key

## props
1. the property of this component
2. assign the property value by v-bind
3. you can use the value in the template by {{ props_item }} format

# Some package

## bulma

I think, it's alot of predefined css class for developor to use

* reference
    * [intro-of-bulma-css-framework](https://askie.today/intro-of-bulma-css-framework/)
    
1. you can add css feature theme for a html element by add following tag in class
    * class="content is-small"

## router-view

* reference
    * [introduce](https://ithelp.ithome.com.tw/articles/10214449) 
    * [nested-routers](https://medium.com/unalai/%E8%AA%8D%E8%AD%98-vue-router-%E5%B5%8C%E5%A5%97%E8%B7%AF%E7%94%B1-nested-routes-8168f5395941)

* Generally, we use [url -> route -> component] to set our routing in route.ts
* you should add router-view compont in your component when you want to use router
```
<template>
  <section>
    <router-view></router-view>
  </section>
</template>
```
* if you use nested routers, you should add router-view in both parent and child component