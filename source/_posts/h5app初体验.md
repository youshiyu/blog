---
title: h5app初体验
date: 2020-05-13 02:16:20
tags:
---
### 云打包 ###

使用hbuildx的云打包功能，打包h5安卓app，将两个月前做的2048适应手机并打包，调整好格式之后，申请安卓证书，很快就打包好了apk

### 遇到的坑 ###

使用webpack打包的时候，发现index.html的文件没有引号，查找相关信息是因为webpack的build下有个webpack.prod.conf.js文件的minify这个对象有个removeAttributeQutotes的属性，删除引用的意思，这个值默认是true,改成false

### webpack把js引入index.html的过程 ###

vuecli3和vuecli2在配置上有很大不同，配置相关信息在@vue/cli-service中

   
    问题一：压缩文件中过滤了“ ”，需要在@vue/cli-service/lib/config中配置，之前的removeAttributeQutotes属性位置在app.js中minify对象中

    问题2：路由跳转配置是，最开始是history,打包后，路由跳转失败，改成hash就成功了，查阅相关资料，history需要相关配置。

*总结：hash模式浏览器只会发送http://localhost:8000/请求，前端路由进行跳转，但是在history模式下，在后端没有直接配置例如http://localhost:8000/login等资源，就会造成路由跳转失败*