# 自定义模块

对于自定义的文件模块，需要通过文件的路径来对模块进行引入，路径可以是绝对路径，如果是相对路径必须以`./`或 `../`开头。

```javascript
// 自定义模块
var router = require("./router");
```

### 例子

当exports多个属性和方法时，在require导入时，需要于相应的属性和方法名称相同。

```javascript
// moduleA.js
exports.x = "moduleA.js";
exports.sayHello = function () {
    console.log("moduleA.js say hello....");
}
```

第一种情况：

```javascript
// index.js 该Js文件导入其他模块
var {y, say} = require("./moduleA.js");// <= Error, 必须与moduleA.js的名称相同
var {x, sayHello} = require("./moduleA.js");
console.log(x); // moduleA.js
sayHello(); // moduleA.js say hello ....
```

第二种情况：

```javascript
// index.js 
// 使用一个变量接收modeluA.js，会自动封装为一个对象
var moduleA = require("./01.hello");
console.log(moduleA.x);
moduleA.sayHello();
```