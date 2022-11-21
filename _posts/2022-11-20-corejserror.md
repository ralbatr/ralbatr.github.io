---
title: corejs报错
author: ralbatr
date: 2022-11-20 15:05:28 +0800
categories: [技术、前端]
tags: [随笔]
toc: true
---

重新安装的项目依赖，运行报错/modules/es.array.push.js

```
These dependencies were not found:

* core-js/modules/es.array.push.js in ./node_modules/@babel/runtime/helpers/esm/regeneratorRuntime.js, ./node_modules/cache-loader/dist/cjs.js??ref--12-0!./node_modules/babel-loader/lib!./node_modules/cache-loader/dist/cjs.js??ref--0-0!./node_modules/vue-loader/lib??vue-loader-options!./src/components/Breadcrumb/index.vue?vue&type=script&lang=js& and 11 others
* core-js/modules/es.array.unshift.js in ./node_modules/cache-loader/dist/cjs.js??ref--12-0!./node_modules/babel-loader/lib!./node_modules/cache-loader/dist/cjs.js??ref--0-0!./node_modules/vue-loader/lib??vue-loader-options!./src/views/table/tabFirst/TabFirst.vue?vue&type=script&lang=js&, ./node_modules/cache-loader/dist/cjs.js??ref--12-0!./node_modules/babel-loader/lib!./node_modules/cache-loader/dist/cjs.js??ref--0-0!./node_modules/vue-loader/lib??vue-loader-options!./src/views/table/tabSecond/TabSecond.vue?vue&type=script&lang=js&
* core-js/modules/es.error.cause.js in ./node_modules/@babel/runtime/helpers/esm/regeneratorRuntime.js, ./src/utils/request.js and 1 other
* core-js/modules/es.object.proto.js in ./node_modules/@babel/runtime/helpers/esm/regeneratorRuntime.js
```

* **移除 node_modules**
  * ```
    npm rm -rf node_modules
    ```
* **先安装 core-js**
  * ```
    npm install --save core-js
    ```
* **再重新安装 依赖**
  * ```
    npm install
    ```

    > **原文链接：**[https://stackoverflow.com/questions/72341491/module-not-found-error-cant-resolve-core-js-modules-es-error-cause-js](https://stackoverflow.com/questions/72341491/module-not-found-error-cant-resolve-core-js-modules-es-error-cause-js)
    >

**成功**

Google一下，在stackoverflow看到问题描述的跟我遇到的一样，解决方法是

我试了，都不通。

* 重新 install
* 配置 babel，在babel.config.js中添加：presets: [ [ "@vue/app", { useBuiltIns: "entry" } ] ]

搜了一下，网上给的解决方案有两种
