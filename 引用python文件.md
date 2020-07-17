### 会搜索哪些地方

当我们导入一个模块时：import  xxx，默认情况下python解析器会搜索如下三个部分：

- 当前目录
- 已安装的内置模块
- 已安装的第三方模块

如果在这三个路径都搜索不到这个包，则会报错。



### 查看当前都有哪些搜索路径

搜索路径存放在**sys模块的path**中，可以通过以下代码查看当前的path有哪些：

```
import sys
print(sys.path)
```



### 添加搜索路径

需要注意import的python文件路径是否在sys.path中，如果不存在，则需要我们手动添加到sys.path中，代码如下：

```
sys.path.append(python_file_path)
```

