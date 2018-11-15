---
title: vue -- Cannot set property 'render' of undefined解决方法
date: 2018-11-15 17:21:11
tags: vue
---
#### 前言
在用vue-cli3做组件测试时，出现个问题，记录一下

报错如下 Cannot set property 'render' of undefined

#### 解决方案
后来发现是因为 组件里写了script标签，没写 export default {}

加上这句话之后就好使了


---


我的个人博客地址：[http://www.xiaolongwu.cn](http://www.xiaolongwu.cn)

github资源地址：[vue -- Cannot set property 'render' of undefined解决方法](https://github.com/LeonWuV/FE-blog-repository/blob/master/vue/vue%20--%20Cannot%20set%20property%20'render'%20of%20undefined%E8%A7%A3%E5%86%B3%E6%96%B9%E6%B3%95.md)

我的CSDN博客地址：[https://blog.csdn.net/wxl1555](https://blog.csdn.net/wxl1555)

如果您对我的博客内容有疑惑或质疑的地方，请在下方评论区留言，或邮件给我，共同学习进步。

邮箱：wuxiaolong802@163.com