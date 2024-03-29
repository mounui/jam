---
title: Hexo在Github托管的博客绑定个人域名
date: 2024-01-05 17:08:25
tags: [hexo,github,域名,博客]
---

拥有独特的域名可以帮助你建立和提升你的在线身份和个人品牌。它作为你网络存在的一部分，使你的网站看上去更加专业。

<img src="https://res.mounui.com/2024/4cd7ceaa7a523971d8889c07f00eba51efef2a.jpg" alt="1ff04428433a4f848a00b1b6a10bf313.png~tplv-6bxrjdptv7-image" style="zoom: 67%;" />

## 一、购买与配置个人域名

这个部分需要基于你选择的域名供应商有所不同。完成购买你喜欢的域名之后，你需要为你的GitHub Pages设置一个自定义域名。大部分供应商提供DNS设置，在该设置页，你需要添加几条记录作为下一步的准备。

旁注：通常，域名服务供应商在其文档或帮助中心提供具体的DNS管理指南。

## 二、添加CNAME文件

在你的Hexo站点源码的`source`目录下新建一个名为`CNAME`的文件，并在该文件中填写你购买的域名。格式如下：

```
your-domain.com
```
保存并关闭文件。

## 三、更改DNS设置

接下来你需要根据你的选择进行域名解析的配置，通常你需要更改DNS设置来指向你的GitHub Page。

一般来说，你需要进行以下操作：

* 必须为每个GitHub Pages的IP地址添加`A`记录。目前GitHub Pages的IP地址如下：
  * 185.199.108.153
  * 185.199.109.153
  * 185.199.110.153
  * 185.199.111.153

* 若你希望通过`www.your-domain.com`访问你的网站，你还需要添加一个`CNAME`记录，该名称为"www"，并将"目标"，"地址"或"值"指定为`your-username.github.io`。

## 四、填写自定义域名

在你的GitHub仓库设置页面找到"GitHub Pages"区域，在"Custom domain"中填写你购买的域名，例如 `your-domain.com`。

点击"Save"按钮保存设置。

## 五、强制https

在GitHub页面中，选中"Enforce HTTPS"选项，这会保护你的博客连接的安全。

经过上述设置后，你就完成了个人域名的绑定，通常需要几个小时到24小时以完成DNS传播。传播完成后，你的博客就可以通过你的自定义域名进行访问了。