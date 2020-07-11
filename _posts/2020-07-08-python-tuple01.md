---
title: 파이썬 데이터 타입 - 리스트, 튜플
categories:
- PYTHON
---

### 리스트
- 순서 중복 수정 삭제 o


```
#### 선언
a = []
b = list()
c = [1, 2, 3, 4]
d = [10, 100, 1000, 'pen', 'banana']
e = [10, 100, 1000, ['pen', 'banana', 'apple', 'mellon']]

#### 인덱싱
print(d[3])
print(d[-2])
print(d[0] + d[1])
print(e[3][1])
print(e[-1][-2])

#### 슬라이싱
print(d[0:3])
print(e[3][1:3])

#### 연산
print(c+d)
print(c * 3)
print(str(c[0]) + ' hi')

#### 리스트 수정, 삭제
c[0] = 77
print(c)  // 결과: [77, 2, 3, 4]

c[1:3] = [100, 1000, 10000] 
print(c) // 결과: [77, 100, 1000, 10000, 4]

c[1] = ['a', 'b', 'c']
print(c) // 결과 : [77, ['a', 'b', 'c'], 1000, 10000, 4]

del c[1]
print(c) // 결과: [77, 1000, 10000, 4]

```

#### 기억하면 좋을 것
- list 함수에서 `del`일 때는 인덱스를 지웠지만 `remove`는 해당 숫자를 지운다
- list 함수에서 `append`는 그 자체가 들어가고 (배열인 경우 배열이 들어감), `extend`는 원소가 들어간다 (배열 안의 원소들만)

### 튜플

- 순서, 중복 O
- 수정, 삭제 x


```
#### 선언
a = ()
b = (1,)
c = (1, 2, 3, 4)
d = (10, 100, ('a', 'b', 'c'))

print(c[2])
print(c[3])
print(d[2][1])
print(d[2:]) // d의 index 2부터 다 나와
print(d[2][0:2])
print(c + d)
print(c * 3)
```

- 튜플 함수

```
z = (5, 2, 1, 3, 7, 1)
print(z)
print(3 in z) // z 변수에 3이 있니
print(z.index(7)) // 7의 인덱스 값은 뭐니
print(z.count(1)) // 1의 갯수
```
