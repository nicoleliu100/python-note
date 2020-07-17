Before executing code, Python interpreter reads source file and define few special variables/global variables.

在执行代码前，python解释器会读取source文件，并定义几个特殊的全局变量。



If the python interpreter is running that module (the source file) as the main program, it sets the special __name__ variable to have a value **“\__main__”**. If this file is being imported from another module, \__name__ will be set to the **module’s name.** Module’s name is available as value to \__name__ global variable.

- 如果python 解释器将某个文件作为主程序运行，则会把特殊变量“\_\_name\_\_”赋值为\__main__。所以下面的代码中，if的条件是满足的，故if 后面的代码会被执行。 _
- _如果这个文件被其他文件import进来，“\_\_name\_\_”就会被设置为这个模块的名字。



举个例子：下面是文件名为 test.py的内容：

```
print "Always executed"
  
if __name__ == "__main__": 
    print ("Executed when invoked directly")
else: 
    print ("Executed when imported")
```

 

如果这个文件直接被执行，那么全局变量 name == main

如果这个文件被引入到其他文件中，那么全局变量 name == test （test为该文件的名字）。



当我们执行一个python文件时：python + script.py

所有缩进为0级的代码都会被执行。





> if __name__ == “main”: is used to execute some code **only** if the file was run directly, and not imported





https://www.geeksforgeeks.org/what-does-the-if-__name__-__main__-do/