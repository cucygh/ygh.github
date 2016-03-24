---
title: 移动Web一体化解决方案
tag: vue
category: MVVM
---
### 什么是Web一体化

一体化就是通过一系列方法解决一个完整的问题。Web一体化就是用不同的技术手段共同解决开发、协同、测试、发布等问题。
本文描述的移动Web一体解决方案是以Vue.js为中心完成VM的操作，使用组件和指令封装核心模块，用NPM管理模块，Webpack编译打包，Sass编译。




### 一体化的构成

<img src="/imgs/custom/vue-solution.png" alt="一体化构成" width="250">

- 路由方案
    一个项目通常是由多个页面组成的，我们把页面的地址的切换方式叫路由。每个页面对应server的一个map地址不妨叫多页面路由、多个页面对应Server的一个map地址叫做单页面路由。在我们这个方案中是两种方案结合的，结合的原则是按业务的紧密程度。比如订单页和支付页作为单页面。
- JS实时编译
    为了提高代码的可维护性和支持协同开发，通常采用模块化开发，在生产环境中需要实时编译Js，本方案采用Webpack实时编译的方式。
- Sass实时编译
    本方案采用Yo作为Css框架，Yo是采用Sass开发的，在生产环境中需要实时编译Sass，本方案采用Sass编译工具来实现。
- 包管理
    组件式开发可以对开发高幅度解耦，本方案使用npm对组件包进行管理，开发人员之间通过npm进行组件管理和复用。
- 调试
    使用Vue进行开发的时候，vue会把数据转化为setter和getter的方式，使用原始的Chrome Dev Tools不便观察数据。本方案采用Chrome Vue调试，有助于实时观察数据的变化。

### 工程结构

本方案的工程结构清晰明了，层级简单，如图所示：
<img src="/imgs/custom/structure.png" alt="工程结构" width="250">

让我们看下如何快速开发一个移动端项目，通常效果如下：

<img src="/imgs/custom/result.png" alt="效果图" width="150">

### 源码展示

所有源码展示在[Github](https://github.com/cucygh/vue-component)
