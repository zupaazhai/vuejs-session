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

## Class and style binding
```html
<button v-bind:class="['btn', 'btn-success']">class as array</button>

<button :class="['btn', 'btn-success']">class as array</button>

<button :class="{'btn': true, 'btn-success': isSuccess}">class as object</button>

<button :style="btnStyle()">class as object</button>

<button :style="btnStyleComputed">class as object</button>
```
```javascript
data () {
  return {
    isSuccess: true
  }
},

computed: {
  btnStyleComputed() {
    return {
      color: this.foo ? 'red' : 'blue',
      backgroundImage: 'url(/path/to/image.jpg)'
    }
  }
},

methods: {
  btnStyle() {
    return {
      color: 'red',
      backgroundImage: 'url(/path/to/image.jpg)'
    }
  }
}
```

## Event Binding (v-on or @)
```html

<!-- normal -->
<button v-on:click="onClick">Click Me</button>

<!-- shorthand -->
<button @click="onClick">Click Me</button>

<!-- with modified -->
<button @click.prevent="onClickWithEvent($event)">Click Me</button>
```
```javascript
methods: {
  onClick() {
    alert("Hello")
  },
  
  onClickWithEvent(e) {
    let txt = e.target.innerText
    console.log(txt)
  }
}
```
see more [modifiers](https://vuejs.org/v2/guide/events.html#Event-Modifiers)
