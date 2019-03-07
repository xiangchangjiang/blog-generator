---
title: HTML常用标签
date: 2019-02-25 10:54:26
tags:
---
>本文主要介绍以下几个标签：

- iframe
- a
- form
- button
- input
- select
- table

#### 一、iframe
- 表示嵌套的浏览上下文，有效地将另一个HTML页面嵌入到当前页面中。
- 老标签，用于嵌套页面，一般与a标签配合使用，
```html
<iframe name=xxx src="#" frameborder="0"></iframe>
<a target="xxx" href="http://qq.com">QQ</a>
<a target="xxx" href="http://baidu.com">baidu</a>
```
1. src中可以填写链接，也可以填写相对路径。
2. src填写地址时，可以在页面打开一个新窗口，大小、位置均可调节。
3. a标签中href所指向的页面在name为xxx的窗口打开。



#### 二、a（anchor）
- 可以创建通向其他网页、文件、同一页面内的位置、电子邮件地址或任何其他 URL 的超链接。
- 浏览器会发出get请求，属性为download时，表明该链接是用来下载的。

`<a href="//qq.com">qq</a>`  a标签的无协议绝对地址，继承当前页面使用的协议。

`<a href="#hi">nihao</a>`    锚点，不会发送请求，只在**页面内跳转**。

`<a href="?name=xx">nihao</a>`点击后`?name=xx`会添加到查询网址查询参数中并发起一个get请求。

`<a href="javascript:alert("1")">`**伪协议**，相当将Javascript作为了一个协议，但javascript并不是一个协议，所以取名为伪协议，作用是点击该链接对应的内容时，在当前页面执行一段javascript代码。

`<a href="javascript:;">`实现一个点击后**什么都不做**的功能，不刷新、不跳转……

`<a href="#">`点击后跳转到页面顶端
`<a href="">`点击后刷新页面
`<a href="/..">link</a>`浏览器发起GET/HTTP/1.1的请求。

**target属性**：以下四个关键字的含义
`_self`：默认值，指当前页面加载。
`_blank`：新窗口打开
`_parent`:加载响应到当前框架的HTML4父框架或当前的HTML5浏览上下文的父浏览上下文。如果没有parent框架或者浏览上下文，此选项的行为方式与*_self*相同。
`_top`: IHTML4中：加载的响应成完整的，原来的窗口，取消所有其它frame。 HTML5中：加载响应进入顶层浏览上下文（即，浏览上下文，它是当前的一个的祖先，并且没有parent）。如果没有parent框架或者浏览上下文，此选项的行为方式同*_self*

#### 三、form
表示了文档中的一个区域，这个区域包含有交互控制元件，用来向web服务器提交信息。一般浏览器会发出post请求。
form中一定要有一个提交按钮
`<form action="users" method="">xxxxx<>`
当method="post"时，浏览器回参数放到请求的第四部分。
当method="get"时，参数会出现在网址的查询参数中。
method="post"也可以出现查询参数---->将action="users"改成action="users?xxx=yyy"。
**target属性**同a标签

#### 四、button
表示一个可点击的按钮，可以用在表单或文档其它需要使用简单标准按钮的地方。 默认情况下，HTML按钮的显示样式接近于 user agent 所在的宿主系统平台（用户操作系统）的按钮， 但你可以使用 CSS 来改变按钮的样貌。
`<button type="">xxx</button>`
button中只要不出现`type="button"`,button按钮就具有**提交**功能。type="text"、type="password"……可以，type=""这句不出现也可以。
**通常表单提交方式为`<input type="submit" value="提交">`**

#### 五、input   
input元素用于为基于Web的表单创建交互式控件，以便接受来自用户的数据; 可以使用各种类型的输入数据和控件小部件，具体取决于设备和user agent。
```html
<input name="fruit" type="radio" value="apple">苹果
<input name="fruit" type="radio" value="banana">香蕉
```
当type="radio"时代表这是单选框，可以有许多选项，这些选项的name要设置为同一个值，否则不能实现单选。
使用label标签可以实现**点字选框**。
有两种方法：
方法一：
`<label><input name="fruit" type="radio" value="apple">苹果</label>`
方法二：
`<input name="fruit" type="radio" value="apple" id="xx"><label for="xx">苹果</label>`
这两种方法都是使文字与选框产生关联，使用方案一更为方便。同理，其它type类型的，也可以用这种方式产生关联。

#### 六、select
select元素表示一个控件，提供一个选项菜单
```html
<select name="group">
	<option value="">_</option>
	<option value="1">第一组</option>
	<option value="2">第二组</option>
	<option value="3"  disabled>第三组</option>
	<option value="4"  selected>第四组</option>
<select>
	
```
第三组中的`disabled`用于使这组不能选中。
第四组中的`selected`点开后默认选中的选项。
当首行`<select name="group" multiple>`
multiple表示按住Ctrl或shift可以多选。

#### 七、table
table表示表格数据即通过二维数据表表示的信息。
常用标签有thead tbody tfoot 
th：table header cell 表头
td：table data cell 数据
tr：table raw
表格合并用`border-collapse:collapse;`
colgroup可以指定表格的宽高以及背景色。
```html
<table>
...
	<colgroup border=1>
		<col width=100 bgcolor=red>
		<col width=200 bgcolor=gold>
		....
	</colgroup>
...
</table>
```
其中`<col width=100 bgcolor=red>`设定第一列宽度为100px，背景色为红色。
`<col width=200 bgcolor=gold>`设置第二列宽度为200px，背景色为gold。
……

