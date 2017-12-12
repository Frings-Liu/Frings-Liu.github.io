---
layout:		post
title: 		Gradle中的BuildScript
subtitle:	Gradle中的BuildScript,emmmm
date:		2017-12-07
author:		Frings
header-img:	img/post-bg-swift2.jpg
catalog: 	true
tags:
	- Gradle
---

在创建Gradle的工程的时候经常都会看见这么一个东西叫做:
#### BuildScript
而且里面有repositories和dependencies的代码内容,使我疑惑为什么一个项目会有两个repositories和dependencies,这样不是很奇怪?

答案是:
BuildScript中的申明是gradle脚本自身需要使用的一些资源.
可以申明的内容有:
资源依赖项
第三方插件
maven仓库地址等

---
gradle是由groovy语言编写的，支持groovy语法，可以灵活的使用已有的各种ant插件、基于jvm的类库，这也是它比maven、ant等构建脚本强大的原因。虽然gradle支持开箱即用，但是如果你想在脚本中使用一些第三方的插件、类库等，就需要自己手动添加对这些插件、类库的引用。而这些插件、类库又不是直接服务于项目的，而是支持其它build脚本的运行。所以你应当将这部分的引用放置在buildscript代码块中。gradle在执行脚本时，会优先执行buildscript代码块中的内容，然后才会执行剩余的build脚本。




