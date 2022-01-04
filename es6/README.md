---
sidebar: auto
pageClass: custom-page-class
---

# ECMAScript 6

[ECMAScript 6.0](https://es6.ruanyifeng.com/#docs/intro)（以下简称 ES6）是 JavaScript 语言的下一代标准，已经在 2015 年 6 月正式发布了。它的目标，是使得 JavaScript 语言可以用来编写复杂的大型应用程序，成为企业级开发语言。

## ECMAScript 6 简介

### ECMAScript 和 JavaScript 的关系

ECMAScript 和 JavaScript 的关系是，前者是后者的规格，后者是前者的一种实现（另外的 ECMAScript 方言还有 JScript 和 ActionScript）。日常场合，这两个词是可以互换的

### 什么是 ES6？

ES6 是 ECMAScript 6 的缩写简称。它是 ECMAScript 的第 6 个版本，也就是说它有更早的版本，以后还会有更多版本。

### ES6 与 ECMAScript 2015 的关系

ES6 既是一个历史名词，也是一个泛指，含义是 5.1 版以后的 JavaScript 的下一代标准，涵盖了 ES2015、ES2016、ES2017 等等，而 ES2015 则是正式名称，特指该年发布的正式版本的语言标准。本书中提到 ES6 的地方，一般是指 ES2015 标准，但有时也是泛指“下一代 JavaScript 语言”。

### ES6 浏览器兼容

目前，大部分浏览器对 ES6 的已经支持，详情可以查看https://kangax.github.io/compat-table/es6/

#### Babel 转码器

对于兼容性不好的浏览器，需要使用 [Babel 转码器](https://es6.ruanyifeng.com/#docs/intro#Babel-%E8%BD%AC%E7%A0%81%E5%99%A8)进行转码，可以将 ES6 代码转为 ES5 代码，从而在老版本的浏览器执行。这意味着，你可以用 ES6 的方式编写程序，又不用担心现有环境是否支持。

#### 命令编译转码

代码编译时，通过执行工具@babel/cli，用于命令行转码

#### 浏览器运行时转码

Babel 也可以用于浏览器环境，使用@babel/standalone 模块提供的浏览器版本，将其插入网页。

```html
<script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
<script type="text/babel">
  // Your ES6 code
</script>
```

注意，网页实时将 ES6 代码转为 ES5，对性能会有影响。生产环境需要加载已经转码完成的脚本。

Babel 提供一个[REPL 在线编译器](https://babeljs.io/repl/)，可以在线将 ES6 代码转为 ES5 代码。转换后的代码，可以直接作为 ES5 代码插入网页运行。
