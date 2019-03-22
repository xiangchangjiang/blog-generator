---
title: JS里的数据类型转换
date: 2019-03-20 23:32:01
tags:
---
## JS 里的数据类型转换
- 这篇文章包括以下内容：
- number转string
- 其它类型转布尔值
- 其它类型转number
- JavaScript数据存储
- 深拷贝和浅拷贝---笔记


#### 一、number转string
三种方法：
1. `(xx).toString()`
2. `window.String(xx)`可以简写为`String(xx)`
3. `xx+''`

这里typeof(xx)="number",推荐使用第三个方法。


#### 二、其它类型转化成布尔值
两种方法：
```javascript
Boolean()
!!()
```
    Boolean(0)
    false
    Boolean(1)
    true
    Boolean('0')
    true
    Boolean('')
    false
    !!1
    true
    !!0
    false
    +'-1'
    -1

falsy值
六个值为false的布尔值，只有这六个，其他值都为true。
-undefined
-null
-false
-0
-NaN
-""或''（空字符串）

#### 三、其它类型转换成number
五种方法：
```javascript
 Numbera('1')//1
 parseInt('1',10)//1  10表示十进制
 parseFloat('1.23')//1.23
 '1'-0//1
 +'-1'//-1
```

#### 四、JavaScript数据存储
数字64位
字符16位
Stack栈 Heap堆
值 简单 存stack //string，除了object
复杂 存heap，地址存在stack(引用)


#### 五、深拷贝和浅拷贝---笔记
栈（stack）为自动分配的内存空间，它由系统自动释放；
堆（heap）则是动态分配的内存，大小不定也不会自动释放。

