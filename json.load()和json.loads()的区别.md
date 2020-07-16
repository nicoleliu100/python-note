[toc]

## 二者区别

- json.load()入参是file

- json.loads()入参是string （ `json.loads`()  函数的参数是string）



## 读取一个json文件的过程

文件名：test.json

文件内容：{'a': 'a', 'b': 'b'}

### 方式1：使用json.load

```
import json
with open("feature_encoder.json","rb") as f:
    print(json.load(f)) 
```

输出：{'a': 'a', 'b': 'b'}

### 方式2：使用json.loads

```
import json
with open("feature_encoder.json","rb") as f:
    # f.read() Read and return up to n bytes.
    print(json.loads(f.read())) 
```

输出：{'a': 'a', 'b': 'b'}



## 有时候会遇到的报错信息

 有时因为传递给 json.loads 的参数不符合 JSON 格式，所以抛出异常

> JSONDecodeError: Expecting value: line 1 column 1 (char 0)

不符合 JSON 格式的原因常见的有：

- 键值对使用单引号而非双引号。

- 参数为（或含有）普通的字符串格式（plain or html）。