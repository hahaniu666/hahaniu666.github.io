---
layout: post
title: 安装jekyll
category: 技术
tags: rvm,ruby,jekyll
description: 搭建自己的博客
---

### 1.第一步：安装rvm

>  rvm可以让你拥有多个版本的Ruby，并且可以在多个版本之间自由切换, 类似nvm

``` 
 curl -L get.rvm.io | bash -s stable
 source ~/.rvm/scripts/rvm
```

等待终端加载完毕,然后后输入：
```
    rvm -v
```
如果能显示版本号则安装成功。

### 2.第二步：安装ruby

首先列出ruby可安装的版本信息
```
    rvm list known
```    
然后安装一个ruby版本
```
    rvm install 2.1.4
```    
如果想设置为默认版本，可以
```
    rvm use 2.1.4 --default
```    
查看已安装的ruby
```
    rvm list
```    
卸载一个已安装ruby版本
```
    rvm remove 2.1.4
```    
### 3.第三步：更换镜像源

查看已有的源
```
    gem source
```    
显示会如下：
```
    CURRENT SOURCES
    http://rubygems.org/
```    
然后我们需要来修改更换源（由于国内被墙）所以要把源切换至淘宝镜像服务器 在终端执行以下命令,如果更改不成功那就直接用吧

``` 
 gem update --system
 gem uninstall rubygems-update
 gem sources -r http://rubygems.org/
 gem sources -a http://ruby.taobao.org
```
### 4.第四步：
安装好ruby 更新完gem后，就可以执行 gem install jekyll 了...

### 参考：
* [https://www.cnblogs.com/lucky-star-star/p/5810630.html](https://www.cnblogs.com/lucky-star-star/p/5810630.html)

### 接下来安装jekyll

### 参考：
* 官网 [https://www.jekyll.com.cn/](https://www.jekyll.com.cn/)
* 主题 [http://jekyllthemes.org/](http://jekyllthemes.org/)
