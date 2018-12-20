---
title: eslint -- Adjacent JSX elements must be wrapped in an enclosing tag
date: 2018-12-17 14:55:10
tags: eslint
---
#### 前言
关于eslint的问题太多了，我们只能慢慢的一个一个的踩坑。

#### 错误信息
Parsing error: Adjacent JSX elements must be wrapped in an enclosing tag. 

这样的错误信息提示eslint配置的问题，如下图
![错误信息](https://raw.githubusercontent.com/LeonWuV/ftp/master/pictures/eslint/eslintFragment.jpg)
#### 解决办法
修改eslint配置文件


```
// 将

"parser": "babel-eslint",

// 改为如下
"parserOptions": {
    "parser": "babel-eslint"
},

```

###### 即如下图所示
![image](https://raw.githubusercontent.com/LeonWuV/ftp/master/pictures/eslint/1545015106.jpg)

最后再附上github的issues链接，[github原issues链接](https://github.com/vuejs/eslint-plugin-vue/issues/186)

---


github资源地址：[eslint -- Adjacent JSX elements must be wrapped in an enclosing tag](https://github.com/LeonWuV/FE-blog-repository/blob/master/webpack/eslint%20--%20Adjacent%20JSX%20elements%20must%20be%20wrapped%20in%20an%20enclosing%20tag.md)

我的CSDN博客地址：[https://blog.csdn.net/wxl1555](https://blog.csdn.net/wxl1555)

如果您对我的博客内容有疑惑或质疑的地方，请在下方评论区留言，或邮件给我，共同学习进步。

邮箱：wuxiaolong802@163.com