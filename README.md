#简单的vue-router
根据不同的url地址，对应不同的内容！

vue官方提供了一个路由插件，可以非常方便的实现路由功能vue-router

路由在vue中的效果：根据hash地址不同，展示不同的组件！

1.创建组件的构造对象
```javascript
var login = {
    template:"<h1>登录</h1>"
}

var register = {
    template:"<h1>注册</h1>"
}

```
2.将组件和hash地址一一对应
```javascript
var router = new VueRouter({
     routes:[
         {
             path:"/login",
             component:login
         },
         {
             path:"/register",
             component:register
         }
     ]
})
```
3.将路由对象和vue实例进行关联
```javascript
var vm =new Vue({
    router:router,
    el:"#app",
})

```
