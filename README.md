# VueJS-TODO-App

About Vue.js
============
Progressive framework for building UI

Declarative Rendering
=====================
Enables to declaratively render data to DOM using simple template

<pre>
div id="app
  {{message}}
/div

var app = new Vue({
  el: '#app',
  data: {
    message: 'Hello Vue!'
  }
})
</pre>

If we change the data of app.message the DOM will be dynamically updated.

Directives
==========

v- to indicate the special attribute
<br>
Example: v-bind

<pre>

div id="app-2"
  span v-bind:title="message" // this can be replaced with :title 
    Hi !
  /span
/div

</pre>

v-if 
<br>
we can bind data to not only text and attributes, but also the structure of the DOM

<pre>

div id="app-3"
  span v-if="seen" Now you see me /span
/div

</pre>

v-for

To add an item to the below list use <code> app4.todos.push({ text: 'New item' }) </code>

<pre>
div id="app-4"
  ol
    li v-for="todo in todos"
      {{ todo.text }}
    /li
  /ol
/div

var app4 = new Vue({
  el: '#app-4',
  data: {
    todos: [
      { text: 'Learn JavaScript' },
      { text: 'Learn Vue' },
      { text: 'Build something awesome' }
    ]
  }
})

</pre>

Handling User Inputs
====================
v-on : Attach event listeners to invoke method

<pre>
div id="app5"
  p {{message}} /p
  button v-on:click="reverseMessage" Reverse Message /button
/div
 
var app5= new Vue({
  el: "#app5",
  data: {
    message: "Hello"
  },
  methods: {
    reverseMessage: function(){
      this.message = this.message.split('').reverse().join('');
    }
  }
}) 

</pre>

In the above example state of the app is changed without touching the dom

Two-way binding
===============
v-model : Two-way binding between form input and app state

<pre>
div id="app6"
  p {{message}} /p
  input v-model="message"
 /div 
</pre>

Components
==========
- Small, Self-contained, Reusable
- View instance with Pre-defined options

<pre>
Vue.Component('todo-item',{
  template: 'li This is todo list /li'
})

ol
    todo-item /todo-item
/ol
</pre>








<pre>
# todo-app

> A Vue.js project
https://scotch.io/tutorials/build-a-to-do-app-with-vue-js-2

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report

# run unit tests
npm run unit

# run e2e tests
npm run e2e

# run all tests
npm test
```

For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

</pre>

