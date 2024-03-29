## 1. replace

replace는 문자열을 변경하는 함수이다. 문자열 안에서 특정 문자를 새로운 문자로 변경하는 기능을 가지고 있다. 사용 방법은 '변수. replace(old, new, [count])' 형식으로 사용한다.

- old : 현재 문자열에서 변경하고 싶은 문자

- new: 새로 바꿀 문자

- count: 변경할 횟수. 횟수는 입력하지 않으면 old의 문자열 전체를 변경한다. 기본값은 전체를 의미하는 count=-1로 지정되어있다. 

```python
a = 'hello world'
a = a.replace('hello','hi')
print(a)

#= 'hi world'
```



## 2. join

**''.join(리스트)**

**'구분자'.join(리스트)**

join 함수는 매개변수로 들어온 리스트에 있는 요소 하나하나를 합쳐서 하나의 문자열로 바꾸어 반환하는 함수입니다.

- ''.join(리스트)
  ''.join(리스트)를 이용하면 매개변수로 들어온 ['a', 'b', 'c'] 이런 식의 리스트를 'abc'의 문자열로 합쳐서 반환해주는 함수인 것입니다.

- '구분자'.join(리스트)
  '구분자'.join(리스트)를 이용하면 리스트의 값과 값 사이에 '구분자'에 들어온 구분자를 넣어서 하나의 문자열로 합쳐줍니다.
  '_'.join(['a', 'b', 'c']) 라 하면 "a_b_c" 와 같은 형태로 문자열을 만들어서 반환해 줍니다.

```python
a = ['h','e','l','l','o']
print(''.join(a))

#= 'hello'
```



## 3. split()

```python
a = "Life is too short"
a.split()

#= ['Life', 'is', 'too', 'short']

b = "a:b:c:d"
b.split(':')

#= ['a', 'b', 'c', 'd']
```

split 함수는 `a.split()`처럼 괄호 안에 아무 값도 넣어 주지 않으면 공백(스페이스, 탭, 엔터 등)을 기준으로 문자열을 나누어 준다. 만약 `b.split(':')`처럼 괄호 안에 특정 값이 있을 경우에는 괄호 안의 값을 구분자로 해서 문자열을 나누어 준다. 이렇게 나눈 값은 리스트에 하나씩 들어가게 된다. `['Life', 'is', 'too', 'short']`나 `['a', 'b', 'c', 'd']`가 리스트인데 02-3에서 자세히 알아볼 것이니 여기에서는 너무 신경 쓰지 않아도 된다.

위에서 소개한 문자열 관련 함수는 문자열 처리에서 사용 빈도가 매우 높고 유용하다. 이 외에도 몇 가지가 더 있지만 자주 사용되지는 않는다.



## 4. index

```python
a = "Life is too short"
a.index('t')

#= 8
a.index('k')

#= Traceback (most recent call last):
   File "<stdin>", line 1, in <module>
   ValueError: substring not found
```

문자열 중 문자 t가 맨 처음으로 나온 위치를 반환한다. 만약 찾는 문자나 문자열이 존재하지 않는다면 오류를 발생시킨다. 앞의 find 함수와 다른 점은 문자열 안에 존재하지 않는 문자를 찾으면 오류가 발생한다는 점이다.



## 5. strip



### 왼쪽 공백 지우기(lstrip)

```
a = " hi "
a.lstrip()

#= 'hi '
```

문자열 중 가장 왼쪽에 있는 한 칸 이상의 연속된 공백들을 모두 지운다. lstrip에서 l은 left를 의미한다.

### 오른쪽 공백 지우기(rstrip)

```
a= " hi "
a.rstrip()

#= ' hi'
```

문자열 중 가장 오른쪽에 있는 한 칸 이상의 연속된 공백을 모두 지운다. rstrip에서 r는 right를 의미한다.

### 양쪽 공백 지우기(strip)

```
a = " hi "
a.strip()

#= 'hi'
```

문자열 양쪽에 있는 한 칸 이상의 연속된 공백을 모두 지운다.