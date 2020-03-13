---
layout:     post
title:      Vue+SSR-01
subtitle:   环境准备和项目安装
date:       2020-03-13
author:     __荒城旧梦
header-img: img/post-bg-learn-ts.jpg
catalog: true
tags:
    -Vue
	-SSR
---

## 项目初始化

初始化方法：
    
    npx ctrate-nuxt-app project-name

在这个过程中，按照自己需求选择对象的选项。特别注意：Choose rendering mode这个选项要选 Universal。因为我们做的是SSR


## 让项目支持es6模块方法(export/inport)

1.首先更改项目启动方式为：增加babel启动方式，（package.json）：
	
	"scripts": {
      "dev": "cross-env NODE_ENV=development nodemon server/index.js --watch server --exec babel-node",
      "build": "nuxt build",
      "start": "cross-env NODE_ENV=production node server/index.js --exec babel-node",
      "generate": "nuxt generate"
 	}

2.增加babel启动集（.babelrc）：

	
	{
	  "presets": "es2015"
	}

3.安装babel-preset-es2015插件：

	npm install babel-preset-es2015
