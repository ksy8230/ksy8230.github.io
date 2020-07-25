---
title: 파이썬 - 클래스
categories:
- PYTHON
---

### Self, 클래스, 인스턴스 변수

파이썬에서의 클래스 기본 선언 방식은 다음과 같다.

```
class UserInfo:
    def __init__(self, name, height): // 초기 변수 선언
        self.name = name
        self.height = height

    def user_info_p(self): // 해당 클래스의 메서드 함수
        print('Name: ', self.name)

```
- 클래스를 사용하는 이유는 자바스크립트와 마찬가지로 코드의 재활용을 위해 도입되고, 때문에 클래스를 인스턴스화 시켜서 주로 사용한다.

인스턴스를 만드는 방법은 다음과 같다.

```
user1 = UserInfo('Kim', 165) // user1이라는 인스턴스 선언
user1.user_info_p()  # Name: Kim // 인스턴스로 메서드 함수 호출

```


### Self ? js의 this의 역할
위 코드에서 초기 변수 선언에 사용된 self는 js에서의 this 와 유사한 역할을 한다.
그렇다면 아래 def 함수 두 개의 차이는 뭘까?

```
class SelfTest():
    def function1():  # self 인자 없어서 인스턴스에서 호출 불가능하고 클래스에서 직접 호출해야한다
        print('func1 called')

    def function2(self):  # self가 있으면 인스턴스 함수이다
        print(id(self))
        print('func2 called')

```

즉,
self_test = SelfTest()
self_test.function1() <- 부모 클래스에서 메서드에 self가 없다면 이렇게 호출이 불가하다.
SelfTest.function1() <- 부모 클래스에서 직접 호출을 해야 한다
