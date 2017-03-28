---
title: 文档的使用
date: 2017-03-28 10:31:15
tags:
categories: 系统使用
---

# 该系统是如何使用的

<!-- more -->

## 环境需要

> Node

> Git

> 申请一个Github地址 (咱们的github地址已经创建好)

## 安装HEXO
在工程文件夹中
```
npm install -g hexo
```

## 初始化

```
hexo init
```

所有工作准备完成

***

## 生成静态页

```
hexo generate 或 hexo g
```

## 本地服务启动
用于本地调试
```
hexo server
```
在浏览器里输入http://localhost:4000

## 常见的HEXO配置错误：

```
ERROR Plugin load failed: hexo-server

原因： Besides, utilities are separated into a standalone module. hexo.util is not reachable anymore.

解决方法，执行命令：$ sudo npm install hexo-server --save
```

***

## 配置Github

#### 创建仓库
![](/images/system/step_1.png)

#### 修改配置

进入工程根目录，打开_config.yml，翻到最后一部分，修改如下
```
deploy:
  type: git
  repository: git@github.com:rongge1301/lxfe.github.io.git //远成仓库地址
  branch: master
```
执行如下命令使用git部署
```
npm install hexo-deployer-git --save
```

***

## 部署步骤
每次部署可以按照如下三步
```
hexo clean
hexo g
hexo d
```
一下常用命令
```
hexo new "postName" #新建文章
hexo new page "pageName" #新建页面
hexo generate #生成静态页面至public目录
hexo server #开启预览访问端口（默认端口4000，'ctrl + c'关闭server）
hexo deploy #将.deploy目录部署到GitHub
hexo help  #查看帮助
hexo version  #查看Hexo的版本
```

***

## 显示摘要

> 在文章中加入`<!-- more -->`,之后的文章就不会再首页显示

***

## 分类管理
#### 创建分类
在命令行下输入命令
```
hexo new page "分类名" //例如，cms系统
```

#### 新建文章

```
hexo new "cms"
```

用编辑器打开文章，目录地址/source/_posts/cms.md,所有的文章管理都在此目录下,在代码头部增加

```
---
title: cms系统使用          //标题
date: 2017-03-23 19:11:50
tags:
categories: "cms系统"     //添加一行，问号后面要空一个，设置分类名称
---
```

即可完成归类,为了管理方便，每篇文章都要设置分类

