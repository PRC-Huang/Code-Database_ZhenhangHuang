# Linux 常用高级命令
### 精准杀死某个进程
```bash
  ps -df| grep 'python test.py' | awk '{print $2}' | xargs kill -9
```
1. 找到要终止的启动命令 ```ps -df | grep 'python test.py'```
2. 打印相关该命令的id ``` | awk '{print $2}'```
3. 将命令对应的id传给```| xargs kill -9```, 终止进程
