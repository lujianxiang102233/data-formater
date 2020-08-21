### 安装方法

1、npm 安装

执行命令：`npm install vuedemo-npm-practice`

2、yarn 安装

执行命令：`yarn add vuedemo-npm-practice`

3、使用 vuedemo-npm-practice.js

### 使用方法

1、组件内部使用

html:

```javascript
　　<vuedemoNpmPractice :propData="initData"></vuedemoNpmPractice>
```

js：

```javascript
import vuedemoNpmPractice from "vuedemo-npm-practice";
export default {
  name: "app",
  components: {
    vuedemoNpmPractice
  },
  data() {
    return {
      initData: "Welcome to Your Vue.js App"
    };
  }
};
```

2、 main.js 全局安装：

```
import vuedemoNpmPractice from "vuedemo-npm-practice";
Vue.use(vuedemoNpmPractice);
```

然后在其他.vue 文件里面，直接使用组件 <vuedemoNpmPractice/> 即可

3、直接引用打包后的 vuedemo-npm-practice.js

这种方式就不需要 webpack 这类的构建工具，跟 jquery 的方式差不多，可以直接页面引用，使用方法示例如下：

#### HTML 代码 HTML codes

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
</head>
<body>
<div id="app">
  <vuedemoNpmPractice :propData="propData"></vuedemoNpmPractice>
</div>
<script src="https://unpkg.com/vue/dist/vue.js"></script>
<script src="./dist/vuedemo-npm-practice.js"></script>
<script>
  new Vue({
    el: '#app',
    data: function() {
      return {
        propData: '11111111111111111111'
      }
    },
    methods: {
    }
  })
</script>
</body>
</html>
```
