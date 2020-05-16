---
title: 什么是BFC
date: 2020-04-01 01:02:35
tags:
---
**块格式化上下文（Block Formatting Context，BFC）** 是Web页面的可视化CSS渲染的一部分，是块盒子的布局过程发生的区域，也是浮动元素与其他元素交互的区域。**具有 BFC 特性的元素可以看作是隔离了的独立容器，容器里面的元素不会在布局上影响到外面的元素，并且 BFC 具有普通容器所没有的一些特性。**

满足以下条件的触发BFC特性
- body根元素
- 浮动元素 float：除了none
- 绝对定位元素：absolute，fixed
- display：inline-block，table-cells，flex
- overflow：除了visible


