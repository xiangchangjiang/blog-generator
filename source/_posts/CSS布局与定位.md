---
title: CSS布局与定位
date: 2019-03-07 18:06:55
tags:
---
## CSS布局与定位

本文章主要介绍：如何使用CSS做出

1. 左右布局
2. 左中右布局
3. 水平居中
4. 垂直居中
5. 等其他小技巧


### 一、左右布局
1.float+clearfix
左右标签加上`float:left;`在左右标签的父标签上加上`class="clearfix"`。
2.绝对定位
 用一个relative父元素包裹住所有元素，子元素absoulte调整位置。

### 二、左中右布局
1.float+margin
>![](https://github.com/xiangchangjiang/blog-generator/blob/master/images/%E5%B7%A6%E4%B8%AD%E5%8F%B3%E5%B8%83%E5%B1%801.jpg?raw=true)

2.float+absolute
>![](https://github.com/xiangchangjiang/blog-generator/blob/master/images/%E5%B7%A6%E4%B8%AD%E5%8F%B3%E5%B8%83%E5%B1%802.jpg?raw=true)
资料来源于知乎Bsm


### 三、水平居中
1.父级宽度确定
- 子级宽度不确定：在子级样式上写`margin:0 30px;`
- 子级宽度也确定：在子级样式上写`margin:0 auto;`
>![](https://github.com/xiangchangjiang/blog-generator/blob/master/images/%E6%B0%B4%E5%B9%B3%E5%B1%85%E4%B8%AD%EF%BC%9A%E5%AE%BD%E5%BA%A6-%E7%88%B6%E5%AE%9A%E5%84%BF%E9%9A%8F%E6%84%8F.jpg?raw=true)
ps:在CSS中，宽度和高度值最好都不要给一个定值，给定值后，内部内容有变化时容易出bug。

2.父级设置为`display:flex;`时。
>![](https://github.com/xiangchangjiang/blog-generator/blob/master/images/%E6%B0%B4%E5%B9%B3%E5%B1%85%E4%B8%AD%EF%BC%9A%E7%88%B6%E7%BA%A7-flex.jpg?raw=true)

3.子级设置有`display:inline,inline-*`时。
>![](https://github.com/xiangchangjiang/blog-generator/blob/master/images/%E6%B0%B4%E5%B9%B3%E5%B1%85%E4%B8%AD%EF%BC%9A%E5%AD%90%E7%BA%A7.jpg?raw=true)

### 四、垂直居中
1.父级高度确定，父级设置`display:flex;`时。
无论子级高度是否确定都可以使用`align-items:center`设置子级相对父级垂直居中。
>![](https://github.com/xiangchangjiang/blog-generator/blob/master/images/%E5%9E%82%E7%9B%B4%E5%B1%85%E4%B8%AD%EF%BC%9A%E9%AB%98%E5%BA%A6-%E7%88%B6%E5%AE%9A%E5%84%BF%E9%9A%8F%E6%84%8F.jpg?raw=true)

2.父级高度不确定，
在父级使用`padding:20px 0;`

- 子级高度不确定
>![](https://github.com/xiangchangjiang/blog-generator/blob/master/images/%E5%9E%82%E7%9B%B4%E5%B1%85%E4%B8%AD%EF%BC%9A%E9%AB%98%E5%BA%A6-%E7%88%B6%E5%AD%90%E9%83%BD%E4%B8%8D%E5%AE%9A.jpg?raw=true)

- 子级高度确定
>![](https://github.com/xiangchangjiang/blog-generator/blob/master/images/%E5%9E%82%E7%9B%B4%E5%B1%85%E4%B8%AD%EF%BC%9A%E9%AB%98%E5%BA%A6-%E7%88%B6%E4%B8%8D%E5%AE%9A%E5%84%BF%E5%AE%9A.jpg?raw=true)


### 五、其他小技巧
1.对块级元素设置inline-block时，块级元素宽度收缩
块级元素不写宽度的情况下，默认宽100%（毕竟占据一行）。加入inline-block，宽度自动适合内容
块级元素下方会产生空隙，使用`vertical-align:top;`清除空隙。
```css
display:inline-block;
vertical-align:top;
```
这两者一般一起使用。

2.伪类[ `xxxxxxx xxxxx:nth-child()`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:nth-child " `xxxxxxx xxxxx:nth-child()`")
可以在一个列表中指定选择任意一项，或所有奇数（odd）项、偶数（even）项……
