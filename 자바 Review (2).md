# 자바 Review (2)

~~~
__목차__
1. 연산자
2. 제어문 (조건문과 반복문)
~~~

### 1. 연산자

- 연산자(Operate)란?

  ```
  ▶ 의미 : 어떠한 기능을 수행하는 기호(+,-,*,/ 등)
  ▶ 기능 : 강제형변환, 산술, 비교, 논리, 조건, 대입, 복합대입, 증감
  ```

- 연산자의 종류

  > __1) 단항 연산자 : 연산에 필요한 피연산자가 1개__

  ```
  ▶ +, - (피연산자의 부호를 바꿔주는 부호 연산자)
  ▶ ++, --, ~, !
  ```

  > __2) 이항 연산자 : 연산에 필요한 피연산자가 2개__

  ```
  (1) 산술 : + - * / % << >> >>>
  (2) 비교 : > < >= <= == !=
  (3) 논리 : && || & ^ |
  ```

  > __3) 삼항 연산자 : 연산에 필요한 피연산자가 3개__

  ```
  ▶ : ? :
  ```

  ![1558844539880](C:\Users\kyung\AppData\Roaming\Typora\typora-user-images\1558844539880.png)

![1558844583012](C:\Users\kyung\AppData\Roaming\Typora\typora-user-images\1558844583012.png)



- 연산자의 우선순위

  ![1558845186604](C:\Users\kyung\AppData\Roaming\Typora\typora-user-images\1558845186604.png)

- 증감연산자 (++, --)

  ```
  ▶ 증가연산자(++) : 피연산자의 값을 1 증가시킨다.
  ▶ 감소연산자(--) : 피연산자의 값을 1 감소시킨다.
  ```

  | 전위형 | j =   ++i; | ++i;   j =   i; | 값이   참조되기 전에 증가시킨다. |
  | ------ | ---------- | --------------- | -------------------------------- |
  | 후위형 | j =   i++; | j =   i;   i++; | 값이   참조된 후에 증가시킨다.   |



- 이항연산자의 특징

  - 이항연산자는 연산을 수행하기 전 피연산자의 타입을 일치시킨다.

  > int보다 크기가 작은 타입은 int로 변환한다. (byte, char, short -> int)

  - 피연산자 중 표현범위가 큰 타입으로 형변환 한다.

  ```
  ▶ byte + short → int + int → int 
  ▶ char + int   → int + int → int 
  ▶ float + int   → float + float → float 
  ▶ long + float  → float + float → float 
  ▶ float + double → double + double → double
  ```



- 논리연산자 (&&,  ||)

  - 피연산자가 반드시 boolean이어야 하며 연산결과도 boolean이다.
  -  &&가 || 보다 우선순위가 높다. 같이 사용되는 경우 괄호를 사용하자

  ```
  ▶ OR연산자(||) : 피연산자 중 어느 한 쪽이 true이면 true이다.
  ▶ AND연산자(&&) : 피연산자 양 쪽 모두 true이면 true이다. 
  ```

  | **x** | **y** | **x   \|\| y** | **x   && y** |
  | ----- | ----- | -------------- | ------------ |
  | true  | true  | true           | true         |
  | true  | false | true           | false        |
  | false | true  | true           | false        |
  | false | false | false          | false        |

---



### 2. 제어문 (조건문과 반복문)

### 2.1 조건문 - if, switch

- 조건문은 조건식과 실행될 하나의 문장 또는 블럭{}으로 구성

  ```
  if(조건식) { 문장들 }
  ```

- Java에서 조건문은 if문과 switch문 두 가지 뿐이다.
- if문이 주로 사용되며, 경우의 수가 많은 경우 switch문을 사용할 것을 고려한다.
- 모든 switch문은 if문으로 변경이 가능하지만, if문은 switch문으로 변경할 수 없는 경우가 많다.



#### __1) if문__

- if문은 if, if-else, if-else if의 세가지 형태가 있다.
- 조건식의 결과는 반드시 true 또는 false이어야 한다.

![1558846952726](C:\Users\kyung\AppData\Roaming\Typora\typora-user-images\1558846952726.png)

#### __2) 중첩 if문__

- if문 안에 또 다른 if문을 중첩해서 넣을 수 있다
- if문의 중첩횟수에는 거의 제한이 없다.

![1558846734773](C:\Users\kyung\AppData\Roaming\Typora\typora-user-images\1558846734773.png)



#### __3) switch문__

- if문의 조건식과 달리, 조건식의 계산결과가 int범위 이하의 정수만 가능
- 조건식의 계산결과와 일치하는 case문으로 이동 후 break문을 만날 때까지 문장들을 수행한다.(break문이 없으면 switch문의 끝까지 진행한다.)
- 일치하는 case문의 값이 없는 경우 default문으로 이동한다. (default문 생략가능)
- case문의 값으로 변수를 사용할 수 없다. (리터럴, 상수만가능)

![1558846940833](C:\Users\kyung\AppData\Roaming\Typora\typora-user-images\1558846940833.png)



#### __4) 중첩 switch문__

- switch문 안에 또 다른 switch문을 중첩해서 넣을 수 있다.

- switch문의 중첩횟수에는 거의 제한이 없다.

  ![1558847009906](C:\Users\kyung\AppData\Roaming\Typora\typora-user-images\1558847009906.png)



#### 5) Math.random() 함수

- Math클래스에 정의된 난수(亂數) 발생함수
- 0.0과 1.0 사이의 double값을 반환한다. (0.0<= Math.random()< 1.0)

![1558847141666](C:\Users\kyung\AppData\Roaming\Typora\typora-user-images\1558847141666.png)

![1558847146537](C:\Users\kyung\AppData\Roaming\Typora\typora-user-images\1558847146537.png)

![1558847150567](C:\Users\kyung\AppData\Roaming\Typora\typora-user-images\1558847150567.png)

---



### 2.2 반복문 - for, while, do-while

- 문장 또는 문장들을 반복해서 수행할 때 사용
- 조건식과 수행할 블럭{} 또는 문장으로 구성
- 반복회수가 중요한 경우에 for문을 그 외에는 while문을 사용한다.
- for문과 while문은 서로 변경가능하다.
- do-while문은 while문의 변형으로 블럭{}이 최소한 한번은 수행될 것을 보장한다.



#### __1) for문__

- 초기화, 조건식, 증감식 그리고 수행할 블럭{} 또는 문장으로 구성
- for(;;)  : 무한루프

![1558847400922](C:\Users\kyung\AppData\Roaming\Typora\typora-user-images\1558847400922.png)

![1558847417632](C:\Users\kyung\AppData\Roaming\Typora\typora-user-images\1558847417632.png)

​	

#### __2) 중첩 for문__

- for문 안에 또 다른 for문을 포함시킬 수 있다.
- for문의 중첩횟수에는 거의 제한이 없다.

![1558847484260](C:\Users\kyung\AppData\Roaming\Typora\typora-user-images\1558847484260.png)



#### __3) while문__

- 조건식과 수행할 블럭{} 또는 문장으로 구성

![1558847914070](C:\Users\kyung\AppData\Roaming\Typora\typora-user-images\1558847914070.png)



#### 4) __중첩 while문__

- while문 안에 또 다른 while문을 포함시킬 수 있다.
- while문의 중첩횟수에는 거의 제한이 없다.

![1558847999068](C:\Users\kyung\AppData\Roaming\Typora\typora-user-images\1558847999068.png)



#### __5) do-while문__

- while문의 변형. 블럭{}을 먼저 수행한 다음에 조건식을 계산한다.
- 블럭{}이 최소한 1번 이상 수행될 것을 보장한다.

![1558848032846](C:\Users\kyung\AppData\Roaming\Typora\typora-user-images\1558848032846.png)



#### __6) break문__

- 자신이 포함된 하나의 반복문 또는 switch문을 빠져 나온다.
- 주로 if문과 함께 사용해서 특정 조건을 만족하면 반복문을 벗어나게 한다.

![1558848066557](C:\Users\kyung\AppData\Roaming\Typora\typora-user-images\1558848066557.png)



#### __7)  continue문__

- 자신이 포함된 반복문의 끝으로 이동한다. (다음 반복으로 넘어간다.)
- continue문 이후의 문장들은 수행되지 않는다.

![1558848104245](C:\Users\kyung\AppData\Roaming\Typora\typora-user-images\1558848104245.png)



#### __8)  이름(lable) 붙은 반복문과 break, continue__

- 반복문 앞에 이름을 붙이고, 그이름을 break, continue와 같이 사용함으로써 둘 이상의 반복문을 벗어나거나 반복을 건너뛰는 것이 가능하다.

![1558848182947](C:\Users\kyung\AppData\Roaming\Typora\typora-user-images\1558848182947.png)