## polyfill
Polyfill是一个js库，抚平不同浏览器之间对js实现的差异
github: https://github.com/Modernizr/Modernizr/wiki/HTML5-Cross-Browser-Polyfills

模板语法
自定义组件


## Vue实例
- 数据属性  Object.freeze(obj)  数据仅读
- 有用的实例属性和方法，以$开头，区别于自定义属性
https://cn.vuejs.org/v2/api/#%E5%AE%9E%E4%BE%8B%E5%B1%9E%E6%80%A7
- 实例生命周期钩子
`created、mountd、updated、destroyed`
> 生命周期钩子的`this`上下文指向调用它的Vue实例。所以：不要在选项属性和回调上使用`this`，因为箭头函数是和父级上下文绑定在一起的，`this`不会是预期的Vue实例。

## 模板语法
### 插值
- 底层实现：将模板编译成虚拟DOM渲染函数
- 插值 `v-once`只渲染一次
- 双括号语法将数据解释为普通数据，v-html 将真实的html输出。
### 指令
- 带有`v-`前缀，值预期是单个javascript表达式（v-for例外）
- 职责 ： 当表达式的值变化的时候，响应式的将连带的影响作用于DOM节点
- 修饰符 ： 指出该指令以特殊的方式绑定
- 缩写 ： v-bind:href="url"   --------->   :href="url"
         v-on:click="doSomething" ------>  @click="doSomething"
         所有支持Vue.js的浏览器这些都能正确解析该语法。
> question: 虚拟DOM的概念
> XSS的攻击 https://en.wikipedia.org/wiki/Cross-site_scripting
> 沙盒的概念


