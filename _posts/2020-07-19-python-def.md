---
title: 파이썬 - 람수식 및 람다 (lambda)
categories:
- PYTHON
---

### 함수 정의 방법
```
def 함수명(parameter)
```

### 함수 호출
```
함수명(parameter)
```

### 리턴 값이 없는 함수
```
def hello(value):
    print('hello def', value)

hello("python!") // hello defPython!
```

### 다중 리턴

```
def function_mul(x):
    y1 = x * 100
    y2 = x * 200
    y3 = x * 300
    return y1, y2, y3


val1, val2, val3 = function_mul(100)
print(val1, val2, val3) // 10000 20000 30000
```

### *args, **kwarge : 매개변수가 몇 개가 넘어가는지 모를 때

```
		def args_function(*args):
    # for t in args:
    #    print(t)
    for i, v in enumerate(args):
        print(i, v)
				
		args_function('kim', 'park')
		// 0 kim
		// 1 park

```

#### **kwarge: 매개변수를 딕셔너리로 넘길 수 있다

```
def kwarg_function(**kwargs):
    for k, v in kwargs.items():
        print(k, v)

kwarg_function(name1='kim', name2='park')
// name1 kim
// name2 park
```
