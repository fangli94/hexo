title: 初学HTML总结
date: 2015-08-13 14:38:03
categories: JavaWeb
tags: HTML
---
##HTML简介

HTML是一种标记语言，所有的内容都在`<html></html>`里面，`<html></html>`里面又分为`<head></head>`和`<body></body>`。

###头信息的作用

<!--more-->

1. 可以设置网页的标题

		<title>标题名称</title>

2. 可以通知浏览器使用指定的编码解释html页面，如以下代码将通知浏览器使用utf-8解释该页面

    	<meta http-equiv="content-type" content="text/html;charset=utf-8" />
    	
3. 设置网页的关键字

		<meta name="keywords" content="关键字"/>
		
###body标签

网页的内容应该写在body标签体内

##常用的HTML标签

###标题标签

h1~h6分别对应1级到6级标题

		<h1><h1>
		<h2><h2>
		……   ……
		<h6><h6>

###段落标签

在`<p></p>`标签之间的内容将会单独为一个段落

###水平线标签

使用`<hr/>`标签之后会产生一个水平线，起分隔作用

###换行标签

`<br/>`  换行

###上标、下标标签

上标标签：`<sup></sup>`如2的16次方应写为`2<sup>16</sup>`浏览器显示出来为2<sup>16</sup>。

下标标签：`<sub></sub>`水的化学式应写为`H<sub>2</sub>O`浏览器显示出来为H<sub>2</sub>O。

###原样标签

原样标签为`<pre></pre>`，它会保留标签内的空格和换行符。

###列表标签

列表标签分为有序列表标签和无序列表标签

####有序列表标签

`<ol></ol>  <li></li>`
	
如：

	<ol>
    	<li>火锅</li>
        <li>烤鸭</li>
        <li>烤鱼</li>
    </ol>

将会显示为：
	
<ol>
    <li>火锅</li>
    <li>烤鸭</li>
    <li>烤鱼</li>
</ol>

####无序列表标签

`<ul></ul> <li></li>`

如：

	<ul>
    	<li>木桶饭</li>
        <li>猪脚饭</li>
        <li>白切鸡</li>
    </ul>

将会显示为：

<ul>
    <li>木桶饭</li>
    <li>猪脚饭</li>
    <li>白切鸡</li>
</ul>

###项目标签

`dl dt dd`

如：

	公司的组织结构：
	<dl>
    	<dt>技术总监</dt>
        <dd>码农1号</dd>
        <dd>码农2号</dd>
        <dt>人事总监</dt>
        <dd>妹子1号</dd>
        <dd>妹子2号</dd>
    </dl>

将会显示为:

公司的组织结构：
<dl>
    <dt>技术总监</dt>
    <dd>码农1号</dd>
    <dd>码农2号</dd>
    <dt>人事总监</dt>
    <dd>妹子1号</dd>
    <dd>妹子2号</dd>
</dl>

###行内标签

`<span></span>`

###块标签

`<div><div>`

块标签的内容会独立占一行。

###常用的实体标签

####空格 

`&nbsp`

####小于号  

`&lt;`

####大于号  

`&gt;`

####&      

`&amp;`

####引号    

`&quot;`

####版权    

`&copy;`

####商标    

`&reg;`

###媒体标签

`<embed></embed>`

用于插入一段媒体

常用属性：

- hidden: 用于设置浏览器插件是否隐藏(true / false)

- src: 用于指定媒体路径

###飘动标签

`<marquee></marquee>`

使标签内的内容在屏幕上飘动

常用属性：

- direction： 指定飘动方向

- scrollamount： 设置飘动速度

- loop： 设定飘动的次数

如以下代码的效果:

		<marquee>我飞起来了</marquee>
		
<marquee>我飞起来了</marquee>

###超链接标签

`<a><a>`

常用属性：

- href: 用于指定链接的资源，可以是mailTo协议或者其他协议例如(thunder://)

- target: 设置打开新资源的目标

	- _blank: 在独立的窗口打开资源
	
	- _self: 在当前窗口打开资源

如以下代码：

		<a target="_Blank" href="http://fangli.me">高清无码.avi</a> <br/>
		
效果为:

<a target="_Blank" href="http://fangli.me">高清无码.avi</a> <br/>

###图片标签

`<img></img>`

常用属性：

- width 和 height: 设置图片的宽度和高度

- alt: 如果图片资源无法找到，那么现实相应的描述

###表格标签

- `<table></table>`: 设定表格

- `<tr></tr>`:一行

- `<td></td>`:一行里面的单元格

- `<th></th>`:表头，默认是居中，加粗

- `<caption><caption>`:表格标题

常用属性:

- border: 设置表格的边框

- width 和 height: 设置宽和高

- colspan: 设置单元格占据指定的行数

- rowspan: 设置单元格占据指定的列数

##表单标签

表单标签： 表单标签的作用是用于提交数据给服务器的。
	
表单标签的根标签是`<form>`标签

常用属性：

- action: 该属性是用于指定提交数据的地址。

- method: 指定表单的提交方式。
	
	- get : 默认使用的提交方式，提交的数据会显示在地址栏上。
     
    - post :  提交的数据不会显示在地址栏上。
    
----

###注意:##

表单项的数据如果需要提交到服务器上面，那么表单项必须要有name的属性值。

----

常用的type:

- text：用于输入文本，只有一行

- password：用于输入密码，输入的东西不可见

- radio：用于单选框，多个的name必须一样

- checkbox：多选，多个的name属性也必须一样

- file：用于打开文件，如上传照片

- submit：把内容提交到服务器

- reset：重置

`<textarea></textarea>`用于实现一个输入文本框(多行)，可以用rows和cols指定宽和高

















