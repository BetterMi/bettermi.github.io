---
layout: post
title: "学习BASH Shell"
date: 2016-01-20 10:18:04 +0800
comments: true
categories: study-notes
---
 什么是Shell
 ========
 
 最直观的，从英语单词来看，Shell就是壳子。那么是什么东西的壳子呢？
 
 我们来举个栗子，你想要电脑给你播放一首歌，我们需要有“声卡”这个硬件，否则不会发出声音，但是硬件们如何能知道我让他们干什么呢？那就需要kernel（核心）来控制了，但是话又说回来，kernel听不懂我们说话，我们也没法直接记住kernel的语言，kernel是怎么和我们沟通的呢，这时候就是Shell的用武之地了。Shell像一个壳子一样将kernel包裹在里面，我们只要记住Shell的一些命令，就可以和kernel沟通了。
 看看下图理解一下：
 
![0320bash_1](/images/2016/01/0320bash_1.jpg)
 
 什么是Bash Shell
 ========
 Bash Shell又是什么鬼？其实我们通俗的理解，衣服鞋子有品牌，耐克阿迪神马的，Shell也有各种牌子啊，Bash牌Shell。。。早年的Unix，因为发展者众，所以形成了很多版本的shell，而Linux使用的这一种版本就称为“Bourne Again Shell（简称bash）”。
 
 Bash的优点
 ======
 这里的介绍主要是通过这些优点，我们有哪些使用时的技巧
 
 * 命令编修能力：
 
 	bash能记忆使用过的指令，通过“上下键”就可以找到之前输入的某个指令。我们曾经输入过的指令都记录	在.bash_history文档中。
 * 档案对比补全功能：
 	
 	输入某个指令的前面几个单词之后，按下“tab”键，那么后面的单词就会自动补全了。如果有重复的指令，连续按下两次“tab”键，就会列出所有的重复单词。文件名也同样可以使用“tab”。
 	
 * 命令别名（alias）设定功能：
 	
 	可以设置别名来代替一些繁琐的操作，比如：
 	alias git-pull='git pull team master && git push origin master',以后直接输入git-pull就可以完成git从team远程仓库的master分支拉取最新代码，并且再push到origin仓库的master分支这样一个略繁琐的操作了，是不是非常方便啊~
 	
 Shell环境下的命令
 =======
 
 