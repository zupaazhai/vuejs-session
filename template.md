# Template and syntax
## print
```html
<template>
  <span>{{ myname}}</span>
  
  print html string
  <span v-html="myname"></span>
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