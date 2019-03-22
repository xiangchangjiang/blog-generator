---
title: JS里的数据类型
date: 2019-03-20 15:42:05
tags:
---
## JS 里的数据类型
这篇文章包括以下内容：
- JS的七种数据类型
- string  字符串
- boolean 布尔
- null与undefined的区别
- object  对象的定义以及属性遍历
- JavaScript的两个bug


#### 一、JS的七种数据类型
-number string boolean（原始类型）
-undefined null （特殊）
-symbol（es6）
-object(包含array function)
使用`typeof `可以查看所属类型

#### 二、string  字符串
1.''空字符串长度为0，' '（空格）长度为1
2.多行字符串推荐写法
```javascript
    var s2='12345'+
    	"67890"+
    	"xxxxx"
```

#### 三、boolean 布尔
六个值为false的布尔值，只有这六个，其他值都为true。
-undefined
-null
-false
-0
-NaN
-""或''（空字符串）

#### 四、null与undefined
语法效果几乎没有区别
null===undefined//false
null==undefined//true

##### 区别
Number(null)//0
Number(undefined)//NaN
5+null//5
5+undefined//NaN
-变量没有赋值——undefined
-一个对象object，暂时不想给值——null
一个非对象，暂时不想给值——undefined


#### 五、object  对象
对象就是一组“键值对”（key-value）的集合（哈希表），是一种无序的复合数据集合。
所有key的类型都为string（字符串），''（空字符串）也可以为key值。
对象中的key若不加引号，命名规则同标识符。

##### 删除对象的属性
```javascript
var person={'name':'frank','age':18}

```
![](https://i.loli.net/2019/03/20/5c91e5314fac7.jpg)
使用delete obj（'xxx'）删除对象属性时，对象的key和value都会被删除。

![](https://i.loli.net/2019/03/20/5c91e662ed33d.jpg)
将对象的属性对应的值设为undefined，则只删除对象key对应的value值。

##### 使用for...in 遍历对象的属性
```javascript
var obj = {a: 1, b: 2, c: 3};

for (var i in obj) {
  console.log(obj[i]);
}
// 1
// 2
// 3
```
使用for...in 遍历需要注意两点
>1. 它遍历的是对象所有可遍历（enumerable）的属性，会跳过不可遍历的属性。
2. 它不仅遍历对象自身的属性，还遍历继承的属性。

#### 六、JavaScript的两个bug
- JavaScript 对 UTF-16 的支持是不完整的，由于历史原因（JS出生早），只支持两字节的字符，不支持四字节的字符。
- `function=f(){}`typeof f     //"function" 理论上应为"object",JS中只有七种数据类型，这七种里不包括"function"

### 参考资料：[JavaScript 标准参考教程（alpha），by 阮一峰](http://javascript.ruanyifeng.com/ "JavaScript 标准参考教程（alpha）")



















