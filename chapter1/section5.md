# 模块机制

Node中每个模块运行时，会自动为其添加一个函数：
```javascript
function (exports, require, module, __filename, __dirname) {
  模块中的代码
}
```
**exports**

- 该对象用来将变量或函数暴露到外部

**require**

- 函数，用来引入外部的模块

**module**
- module代表的是当前模块本身
- exports就是module的属性
- 既可以使用 `exports` 导出，也可以使用`module.exports`导出

**__filename**

- 当前模块的完整路径
- 在模块内可以直接使用`__filename`获得模块的完整绝对路径。

**__dirname**

- 当前模块所在文件夹的完整路径
- 在模块内可以直接使用`__dirname`获得模块所在文件夹的完整绝对路径。

> 在文件操作中，使用相对路径是不可靠 的，因为在node中文件操作的路径设计为相对于执行node命令所处的路径。为了解决这个问题，只需要将相对路径转为绝对路径。
>
> `path.join(__dirname, '相对路径')`