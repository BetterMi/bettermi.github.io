---
layout: post
title: "iOS开发中遇到的小问题"
date: 2016-02-18 10:49:56 +0800
comments: true
categories: study-notes
---
  UIImageView添加手势无效
  ======
  
  向UIImageView对象添加UIGestureRecognizer手势的时候发现，手势无法产生响应。查找原因，原来是默认生成的UIImageView对象的userInteractionEnabled、multipleTouchEnabled属性值为NO，将其设置为YES就可以响应手势了。
