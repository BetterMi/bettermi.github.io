---
layout: post
title: "Octopress的一些配置"
date: 2016-01-22 16:13:59 +0800
comments: true
categories: study-notes
---
 添加文章分类
 ======== 

 1. 添加category_list
> git clone https://github.com/tokkonopapa/octopress-tagcloud.git
 2. 将category_list.html和tag_cloud.html放到/source/_includes/asides路径下，将tag_cloud.rb放到/plugins路径下。
 3. 修改_config.yml，在_config.yml文件中找到default_asides，在中括号中添加asides/category_list.html。加入的顺序决定了在侧边栏中显示的顺序。


