# 核心模块—path

<https://nodejs.org/dist/latest-v10.x/docs/api/path.html>

`path.basename(path)`

获取一个路径中的文件名，默认带扩展名



`path.dirname(path)`

获取一个路径中的目录部分



`path.extname(path)`

获取一个路径中的扩展名



`path.isAbsolute(path)`

判断一个路径是否是绝对路径



`path.join([...paths])`

路径拼接



`path.parse(path)` 

将一个路径转为一个对象，对象属性包括：

- root 根目录
- dir 文件目录
- name 文件名
- ext 扩展名
- base 文件名. 扩展名

