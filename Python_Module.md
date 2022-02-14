# Python 常用功能模块
### 获取指令端参数
```python
import argparse
parser = argparse.ArgumentParser("Project 0") # 参数解析器信息
parser.add_argument('--config', type=str, default='configs/net.py', help='the path of config file')
parser.add_argument('--task_id', type=int, default=1, help='index of the task')
```
### 一次性将所有输入参数转化到cfg字典（避免反复赋值）
```python
cfg = {}
for key, value in args.__dict__.items():
        cfg[key] = value
```
