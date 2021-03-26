---
title: 如何搭建github io 博客
author: ralbatr
date: 2021-03-25 10:52:28 +0800
categories: [技术]
tags: [博客]
toc: false
---

> 趁着热乎，简单写一下流程

1、 注册github

2、 新建一个repo，命名 yourBlogName.github.io

3、 到这个repo里，选择setting，下拉，选择theme。此处也可以直接放一个index.html文件

4、 上传文件

5、 输入yourBlogName.github.io，访问即可

6、 如果你想定制自己的主题。 修改主题。我选择的是 https://github.com/cotes2020/jekyll-theme-chirpy/blob/master/docs/README.zh-CN.md 这个主题，基本是按照这个步骤来的

7、 GitHub Pages 的生成

8、 个性化 修改配置文件
<!-- 重新生产博客命令 -->
```
bundle exec jekyll serve
```
9、这样就可以本地测试博客效果了。访问http://127.0.0.1:4000即可

10、github操作，
参考：https://github.com/cotes2020/jekyll-theme-chirpy/blob/master/docs/README.zh-CN.md


## 参考 

https://sspai.com/post/54608