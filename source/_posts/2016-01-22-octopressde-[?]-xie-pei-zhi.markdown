---
layout: post
title: "Octopress的一些配置"
date: 2016-01-22 16:13:59 +0800
comments: true
categories: study-notes
---
 添加文章分类 
 ======== 

 我们想要给文字加一些分类，同时可以按照这些分类来查看文章，要怎么办呢？

 1. 添加category_list

	```git
	git clone https://github.com/tokkonopapa/octopress-tagcloud.git
	```

 2. 将category_list.html和tag_cloud.html放到/source/_includes/asides路径下，将tag_cloud.rb放到/plugins路径下
 
 3. 修改_config.yml，在_config.yml文件中找到default_asides，在中括号中添加asides/category_list.html。加入的顺序决定了在侧边栏中显示的顺序。
 
 新建及修改Page 
 ======= 

 默认的Octopress给我们生成了两个page，如果我们想要新建一些page，可以这样来做：
 
 1. rake new_page['about']
  
 	这样会生成一个/Users/qiyou_hm/octopress/source/about/index.markdown，编辑就可以啦~ 
 	
 2. 在文件/Users/qiyou_hm/octopress/source/_includes/custom/navigation.htm中中加加
 
 	```html
	 <li><a href="{{ root_url }}/about">AboutMe</a></li>
	```
	
 添加链接
 =======
 
 在侧边栏中我们也可以添加一些友情链接，方法如下：
 
1. 在路径/Users/qiyou_hm/octopress/source/_includes/asides下新建文件blog_link.html
 
 ```
 <section>
	<h1>Links</h1>
	<ul>
    	<li>
    	<a href="https://github.com/yl33643/yl33643.github.io">github yl33643.github.io</a>
    	</li>
	</ul>
 </section> 
```
 
 最后要记住，在_config.yml的default_asides array中添加asides/blog_link.html



