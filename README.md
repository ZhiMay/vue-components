# vue-components

> A Vue.js project

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

# run all tests
npm test
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

### eslint ceheck

node_modules/.bin/eslint --fix src/vuex/store.js

## 自定义组件写法：

1. 一个组件一个目录，如Tab,文件下有tab.vue 和index.js
2. 使用: main.js 中

```bash
import Tab from './components/tab'
Vue.use(Tab)
```
