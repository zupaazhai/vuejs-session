# Template and syntax
## print
```html
<template>
  <span>{{ myname}}</span>
  
  <!-- print html string -->
  <span v-html="myname"></span>
</template>
```

## v-if
```html
<template>
  <span v-if="name === 'john'">Hi John</span>
  <span v-else-if="name === 'adam'">Hi adam</span>
  <span v-else>Hi unknow</span>
</template>
```

## v-show
```html
<template>
  <span v-show="name === 'john'">Hi John</span>
</template>
```

## v-for
```html
<template>
  <!-- For loop with array -->
  <ul>
    <!-- v-for loop should has ":key" -->
    <li :key="item.id" v-for="(item, index) in items">item.name</li>
  </ul>
  
  <!-- For loop with number -->
  <ul>
    <li :key="index" v-for="(number, index) in 10">number</li>
  </ul>
</template>
```

## Event Binding (v-on or @)
```html

<!-- normal -->
<button v-on:click="onClick">Click Me</button>

<!-- shorthand -->
<button @click="onClick">Click Me</button>

<!-- with modified -->
<button @click.prevent="onClick">Click Me</button>
```
see more [modifiers](https://vuejs.org/v2/guide/events.html#Event-Modifiers)
