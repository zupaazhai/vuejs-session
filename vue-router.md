# Vue Router

## Install
```javascript
Vue.use(VueRouter)
```

## Init to main.js
```javascript
const routes = [
  { 
    path: '/', 
    name: 'home',
    component: Foo
  },
  { 
    path: '/contact', 
    name: 'contact'
    component: Bar
  }
]

const router = new VueRouter({
  routes // short for `routes: routes`
})

const app = new Vue({
  router
}).$mount('#app')

```

## rounter-link

```html
<router-link to="{name: 'home'}"></<router-link>
```
