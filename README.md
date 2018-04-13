# my-pritice

> about vue vuex vue-router api prictice

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

```

### vue中的v-if与v-show
#### 1.相同处    动态控制DOM元素的显隐
#### 2.区别
#### 1）实现方式：v-if是动态的对DOM树进行添加或删除；v-show是通过控制DOM元素display样式属性的显隐；
#### 2）编译过程：v-if切换有一个局部编译/卸载的过程，切换过程中合适地销毁和重构内部的事件监听和组件；v-show只是简单的基于css样式的切换
#### 3）编译条件：v-if是惰性的，如果初始条件为false,则什么都不做，只有在第一次变为真时才开始局部编译（编译被缓存？编译被缓存后，然后再切换的时候进行局部销毁）；v-show是在任何条件下（首次条件是否为真）都被编译，然后被缓存，而且DOM元素保留
#### 4)性能消耗：v-if有更高的切换消耗；v-show有更高的初始渲染消耗
#### 5）使用场景：v-if适合不大可能改变;v-show适合频换切换。

### Tips:
#### 1)如果v-show作用的元素，css文件中display:none，通过v-show进行设置不能显示该元素；
#### v-show控制显隐，是通过js代码去修改元素的element style，如果value为false，设置display: none;如果value为true，设置display: ''；于是value为true时，只能将element style中的display效果清除，并不能覆盖css中的display效果；如下图所示，value=true时，v-show改变的是element.style，由于无效，显示效果由css文件中的display决定。

#
## CORS 跨域资源共享 全称 （Cross-origin resource sharing）
#### 见文档 http://www.ruanyifeng.com/blog/2016/04/cors.html

#### 背景：浏览器的"同源策略"（same-origin policy），但是需要浏览器和服务器同时支持。目前所有浏览器都支持该功能，IE10+；
#### 整个CORS通讯过程，都是浏览器自动完成，不需要用户参与。对于开发者而言，CORS通信誉同源的AJAX通信没有差距，代码完全一样。浏览器一旦发现AjAX请求跨域，就会自动添加一些附加的头信息，有时还会多出异常附加的请求，但用户无感；因此，实现CORS通信的关键是服务器。只要服务器实现了CORS接口，就可以跨源通信。
#### 允许浏览器向跨源服务器，发出 XMLHttpRequest请求，从而克服了AJAX只能同源使用的限制
### 请求流程
#### 对于简单请求，浏览器直接发出CORS请求。头信息之中，增加一个Origin字段
#### 服务器端需要指定 Access-Control-Allow-Credentials：true
#### 前端必须在Ajax请求中 设置 xhr.withCredentials = true;



















For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

