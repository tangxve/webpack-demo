# loder 实现资源加载

webpack 内部默认只能处理 js 模块代码

- JS 文件 可以通过默认处理（Default Loader） 成为 Bundle.js
- 其他文件 要通过其他 loader 处理成 bundle.js

- JS file ==>  Default Loader ==> Bundle.js

- Other file ==> Other Loader ==> Bundle.js

- css-loader：只是把 css 编译成 一段 css 字符串模块，只会把css模块加载到js中，而并不会使用这个模块

```js
___CSS_LOADER_EXPORT___.push([
  module.id, 
  "body {\r\n  margin: 0 auto;\r\n  padding: 0 20px;\r\n  max-width: 800px;\r\n  background: #f4f8fb;\r\n}\r\n", 
  ""
]);
```

- 添加一个 style-loader 把 css-loader 转换后的结果通过 style 标签追加到页面上。
- style-loader 作用：将 css-loader 中所加载到的所有样式模块，通过创建 style 标签的方式添加到页面上。

- 其实 Webpack 加载资源文件的过程类似于一个工作管道，你可以在这个过程中依次使用多个 Loader，但是最终这个管道结束过后的结果必须是一段标准的 JS 代码字符串。


-
