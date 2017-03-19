# seed-ui

> Mobile UI components for Vue.js.

## 目录说明

* src/components - 存放组件的目录
* src/components/common - 公共组件目录，不直接导出且会被其它组件依赖
* src/index.js - 导出核心库
* src/modal.js - 导出单组件

> 为保证代码冗余，默认导出编译前源码，由用户自己编译打包

## 样式库

* [material](http://www.materialdoc.com/)

## 核心组件

> 组件命名规则，`sd-componentName`

* toast
* loading
* scrollview
* message
* pulldown
* pullup
* infinite-scroll
* switch
* radio
* checklist

## 指令

* v-lazy
* v-scroll

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
```

For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
