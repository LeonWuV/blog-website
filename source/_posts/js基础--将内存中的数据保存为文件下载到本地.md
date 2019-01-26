---
title: js基础--将内存中的数据保存为文件下载到本地
date: 2019-01-26 10:11:14
tags: js基础
---

### 前言
最近在做一个项目，有个需求就是，前端在内存中维护了一个很复杂的json对象，当点击下载按钮时，需要把这个json对象保存到文本中并下载到本地。
### 总结了两种实现方式
假如在我们项目中有个json对象如下：
```
    var jsonObj = {
        name: 'Leon WuV',
        age: 23
    }
```

#### 方式一
当我们点击下载按钮时，调用如下方法
```
function downFlie() {
      // 创建a标签
      var elementA = document.createElement('a');
      
      //文件的名称为时间戳加文件名后缀
      elementA.download = +new Date() + ".tpl";
      elementA.style.display = 'none';
      
      //生成一个blob二进制数据，内容为json数据
      var blob = new Blob([JSON.stringify(jsonObj)]);
      
      //生成一个指向blob的URL地址，并赋值给a标签的href属性
      elementA.href = URL.createObjectURL(blob);
      document.body.appendChild(elementA);
      elementA.click();
      document.body.removeChild(elementA);
}
```
可以看到文件已经下载到本地了

![image](https://raw.githubusercontent.com/LeonWuV/ftp/master/pictures/downFile/1547565350(1).jpg)

我们在打开文件看下内容

![image](https://raw.githubusercontent.com/LeonWuV/ftp/master/pictures/downFile/1547565389(1).jpg)

也没有问题，是刚才我们维护在内存中的哪个json对象

#### 方式二


```
function downFile() {
  var elementA = document.createElement('a');
  
  elementA.setAttribute('href', 'data:text/plain;charset=utf-8,' + JSON.stringify(json1));
  elementA.setAttribute('download', +new Date() + ".tpl");
  elementA.style.display = 'none';
  document.body.appendChild(elementA);
  elementA.click();
  document.body.removeChild(elementA);
}

```

当然第二种方式和第一种方式的结果是完全一样的，感觉第二种方式更为简单。

github资源地址：[js基础--将内存中的数据保存为文件下载到本地](https://github.com/LeonWuV/FE-blog-repository/blob/master/js%E5%9F%BA%E7%A1%80/js%E5%9F%BA%E7%A1%80--%E5%B0%86%E5%86%85%E5%AD%98%E4%B8%AD%E7%9A%84%E6%95%B0%E6%8D%AE%E4%BF%9D%E5%AD%98%E4%B8%BA%E6%96%87%E4%BB%B6%E4%B8%8B%E8%BD%BD%E5%88%B0%E6%9C%AC%E5%9C%B0.md)

我的CSDN博客地址：[https://blog.csdn.net/wxl1555](https://blog.csdn.net/wxl1555)

如果您对我的博客内容有疑惑或质疑的地方，请在下方评论区留言，或邮件给我，共同学习进步。

邮箱：wuxiaolong802@163.com
