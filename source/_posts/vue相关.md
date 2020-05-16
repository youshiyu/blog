---
title: vue相关
date: 2020-04-11 11:35:30
tags:
---

## 作用域插槽 ##
vue实例中，想要拿到子组件的数据，使用作用域插槽，子组件模板：<slot ：data="XXXX"></slot>
实例中
** <slot-scope="slot">
 <v-for="item in slot.data"> **