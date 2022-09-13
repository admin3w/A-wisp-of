# A-wisp-of
```python
import time


# 定义一个获取运行时间的装饰器


def get_time(func):
    def aa():
        time1 = time.time()
        func()
        endtime = time.time() - time1
        print(endtime)

    return aa


@get_time
def func1():
    for i in range(100):
        print(i)


if __name__ == '__main__':
    func1()

```