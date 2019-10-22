# 模块化基础

## 模块的引用

使用`require()`函数引入一个模块

```javascript
var 变量 = require('模块的标识');
```

## 模块的定义

- 在node中一个js文件就是一个模块。
- 默认情况下在js文件中编写的内容，都是运行在一个独立的函数中，外部的模块无法访问。

**导出变量和函数：**

1. 使用`exports`

```javascript
exports.属性 = 属性值;
exports.方法 = 函数;
```

2. 使用`module.exports`

```javascript
module.exports.属性 = 属性值;
module.exports.方法 = 函数;
module.exports = {}; // <= 重点：单独使用exports不能导出一个对象
```

## 模块的标识

模块的标识就是模块的名字或路径。