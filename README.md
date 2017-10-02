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
