# 1.1 함수

## 1.1.1 함수의 정의

<U>한 집합 A의 각 원소가 다른 집합 B의 한 원소에 대응하는 관계의 모임</U>을, 'A에서 B로 대응하는 **함수(function)**'라고 한다.

$$f: A \rightarrow B$$

- 집합 A: 함수의 **정의역(domain)**.

- $f(a)$: 함수 $f$에 대한 $a$의 **사영(image)**.

  각 원소 $a \in A$에 함수 $f$가 대응하는 집합 B의 원소를 어떻게 찾는가 알려주는 규칙이다.

- $f(A)$: 함수의 **치역(range, 또는 codomain)**.

  사영($f(a)$)의 집합으로, $f(A) = \{ f(a)|a \in A \}$이다. ($f(A) \subseteq B$의 포함 관계를 만족한다.)

<br/>

### 1.1.1.1 수식 표현, 독립변수와 종속변수

아래는 함수를 수학적 식으로 표현한 예시다.

$$f(x) = 2x^2 - 1 \,\, 또는 \,\, y = 2 x^2 - 1$$

이때 특별한 언급이 없으면 실수 집합 $\mathbb{R}$의 원소 $x$를 $(2x^2 - 1) \in \mathbb{R}$에 대응하는 함수를 뜻한다.

- 정의역은 $\mathbb{R}$이 되고, 치역은 집합 $\{ 2x ^ 2 - 1 | x \in \mathbb{R} \}$을 의미한다.

- 이때 x를 **독립변수(independence variable)**라 하고, **y를 종속변수(dependent variable)**라 한다.

<br/>

### 1.1.1.2 곱집합

또한 집합 $A \times B = \{ (x,y)|x \in A, y \in B \}$를 두 집합 A, B의 **곱집합(Cartesian product)**이라 할 때, 함수 $f: A \rightarrow B$를 집합 A, B의 원소들의 관계쌍의 집합으로 표현하기도 한다.

$$\{ (a, f(a))| a \in A, f(a) \in B \} \subseteq A \times B$$

이때 함수의 정의, '집합 A의 각 원소는 집합 B의 한 원소에 대응'되정어야 하므로,

> 임의의 두 원소 $a, b \in A$에 대하여 a = b이면 f(a) = f(b)

가 됨을 함수는 항상 만족해야 한다.

<br/>

### <span style='background-color: #393E46; color: #F7F7F7'>&nbsp;&nbsp;&nbsp;예제 1.1.1&nbsp;&nbsp;&nbsp;</span>

- #### 단위함수와 합성함수

원소 $a \in A$를 자기 자신 $a \in A$와 대응하는 함수를 **단위함수(identity function)**라 한다. **항등 함수**라고도 하며 입력이 그대로 출력이 된다.

$$I_{A} : A \rightarrow B$$

```
인공지능에서 연속적인 수치를 예측하는 회귀 문제를 다룰 때, 입력과 출력의 데이터 간 연속성을 유지하기 위해, (Scaling을 위한 Sigmoid, Step function 같은 함수를 사용하지 않고) 항등 함수를 사용했다.(y = x) (입력 = 출력)
```

함수 $f: A \rightarrow B$와 함수 $g: B \rightarrow C$에 대해, 집합 A의 원소 $a \in A$를 원소 $g(f(a)) \in C$로 대응하는 함수를 정의할 때, 이 새 대응함수를 두 함수 $f, g$의 **합성함수(composite function)**이라 한다.

$$g \circ f : A \rightarrow C$$

특히 모든 함수에 대해 단위함수와 합성함수는 함수 자신이 된다.

$$I_{B} \circ f = f = f \circ I_{A}$$

<br/>

- #### 부분집합

함수 $f: A \rightarrow B$이고, A의 부분집합 $D \subseteq A$가 주어졌을 때, $f(D)$는 다음과 같이 표현한다.

$$f(D) = \{ f(x) \in B | x \in D \}$$

<br/>

- #### 전사함수

다음과 같은 함수 $f$를 **전사함수(onto function, surjective function)**라 한다.

$$모든 \, 원소 \, b \in B \, 에 \, 대해 \, b = f(a)가 \, 되는 \, a \in A 가 \, 존재$$

<br/>

- #### 단사함수

대응되는 두 원소가 같으면 정의역의 대등한 원소가 같은 함수 $f$를 단사함수(one-to-one function, injective function)라고 한다.

$$ f(a) = f(b) \, 이면 \, a = b $$

<br/>

- #### 일대일 대응함수(전단사함수)

전사함수이면서 단사함수인 함수를 **일대일 대응함수** 또는 **전단사함수**(one-to-one correspondence function, bijective function)라고 한다.

<br/>

- #### 역함수

함수 $f: A \rightarrow B$에 대한 $a \in A$의 사영인 $f(a) in B$를 다시 원소 $a \in A$에 대응하는 함수로 정의할 수 있다. 이 함수를 함수 $f: A \rightarrow B$의 **역함수(inverse function)**라고 한다.

$$ f^{-1}: B \rightarrow A $$

> 일반적으로 역삼수가 존재할 필요충분조건은 '함수 $f: A \rightarrow B$가 전단사함수를 만족한다'이다.

<br/>

### <span style='background-color: #393E46; color: #F7F7F7'>&nbsp;&nbsp;&nbsp;예제 1.1.2&nbsp;&nbsp;&nbsp;</span>

- #### 내림함수와 올림함수

실수 집합 $\mathbb{R}$과 정수 집합 $\mathbb{Z}$에 대해, $x \in \mathbb{R}$을 넘지 않는 최대 정수에 대응하는 함수를 **내림함수(floor function)**라고 한다.

$$\lfloor \quad \rfloor : \mathbb{R} \rightarrow \mathbb{Z}$$

예를 들어 $\lfloor 4.64 \rfloor = 4$이며 $\lfloor -2.14 \rfloor = -3$이다.

또한 실수 $x \in \mathbb{R}$를 x보다 작지 않은 최소 정수에 대응하는 함수를 **올림함수(ceiling function)**라고 한다.

$$\lceil \quad \rceil : \mathbb{R} \rightarrow \mathbb{Z}$$

예를 들어 $\lceil \sqrt{5} \rceil = 3$이며 $\lceil -8.5 \rceil = -8$이다.

모든 실수 x를 넘지 않는 최대 정수와, x보다 작지 않은 최소 정수는 언제나 존재한다. 따라서 올바르게 정의된 함수라고 할 수 있다.(정의역은 실수 집합 $\mathbb{R}$, 치역은 정수 집합 $\mathbb{Z}$가 된다.) 덕분에 두 함수는 전사집합이라는 조건은 만족하지만, 정수 n에 대응하는 실수가 두 개 이상 존재하므로 단사함수는 아니다.

다시 말해 전단사함수는 아니며, 그러므로 역함수도 존재하지 않는다.

<br/>

- #### 함수 $f(x) = x^{3}$

함수 $f(x) = x^{3}$은 치역의 원소인 실수 $x^{3}$에 대해, 정의역 원소 $\sqrt[3]{x^3}=x$가 유일하게 존재하므로, 전사함수이다. 또한 치역의 두 원소가 $x^3 = y^3$이면 $x = y$이므로 단사함수이다.

즉, 전단사함수이며 역함수 $f^{-1}(x) = \sqrt[3]x$가 존재한다.

<br/>

### 1.1.1.3 배열(수열)

자연수 집합 $\mathbb{N} = \{1,2,3, \cdots \}$ 또는 음이 아닌 정수 집합 $\{0\} \, \cup \, \mathbb{N} = \{1,2,3, \cdots \}$을 정의역으로 하고, 이 정의역 각 수가 어떤 집합 A의 원소에 대응하는 함수를 **배열** 또는 **수열(sequence)**라고 한다. 수열 함수의 치역을 $a_{1}, a_2, a_3, \cdots$ 또는 ${a_n}$로 표시한다.

- 수열의 합: 치역 $a_1, a_2, a_3$이 수의 개념을 가질 때, 수열의 합은 다음과 같이 표시한다.

$$ \sum_{j=1}^{n} {a_j} = a_1 + a_2 + \cdots + a_n $$

- 무한급수: 정의역이 무한개인 수열함수를 무한수열이라 한다. 이 무한수열의 합 $\sum_{j=1}^{\infty}{a_j}$를 **무한급수(inftyite series)**라고 한다.

$$ \sum_{j=1}^{\infty} {a_j} = a_1 + a_2 + \cdots $$

아래는 각각 배열의 합집합과 교집합을 의미한다.

$$ \cup_{n} a_n = a_1 \cup a_{2} \cup \cdots $$

$$ \cap_{n} a_n = a_1 \cap a_{2} \cap \cdots $$

<br/>

### <span style='background-color: #393E46; color: #F7F7F7'>&nbsp;&nbsp;&nbsp;예제 1.1.3&nbsp;&nbsp;&nbsp;</span>

- $\{ a_n\} = \{ (-1)^n \}$ 수열의 합

$\sum_{j=1}^{\infty}a_j = \sum_{j=1}^{\infty}{(-1)^j} = -1+1-1+1-1+ \cdots$는 -1 또는 0으로 발산한다. 

따라서 수열 $\{ a_n\} = \{ (-1)^n \}$의 합은 존재하지 않는다.

<br/>

---

<br/>

## 1.1.2 재귀 함수

다음 두 조건을 만족하는 함수를 **재귀 함수(recursively defined function)**라고 한다.

1. **초기조건**: 정의역 몇 개 원소(기초 원소)의 함수 값이 주어진다.

2. **재귀식**: 기초 원소에 가까운 원소에 대해 자신의 함수 값을 이용하여 함수를 정의한다.

함수의 값을 구할 때 계속 순환하지 않게, 무한히 진행되지 않도록 초기조건이 필요하다. 2번 조건인 재귀 함수 식을 **점화식** 또는 **재귀식(recurrence relation)**이라고 한다. 다시 말하면 함수 값 $a_n$이 n보다 작은 원소들(주로 정수)로 구성된 함수 값들로 정의된다는 의미다.

예를 들어 자연수 n에 대한 수열 함수 $a_n = 2^n$을 재귀함수로 정의하면 다음과 같다.

1. 초기조건: $a_0 = 1$

2. 재귀식: $a_n = 2 \cdot a_{n-1}, n \ge 1 $

<br/>

### <span style='background-color: #393E46; color: #F7F7F7'>&nbsp;&nbsp;&nbsp;정의 1.1.1&nbsp;&nbsp;&nbsp;</span>

- k계 선형 재귀식

$$a_n = c_1a_{n-1} + c_2a_{n-2}+ \cdots + c_ka_{n-k} + f(n), \quad n \ge k$$

k개의 상수 $c_1, c_2, c_3, ..., c_k$에 대해, 위 식과 같이 '선행하는 k개의 함수(또는 수열)에 관한 **1차식**으로 함수 $\{a_n\}$을 정의하는 재귀식을 **k계 선형 재귀식**( $k$ th-order linear recurrence relation)이라고 한다.

- k계 선형 동차 재귀식

$$a_n = c_1a_{n-1} + c_2a_{n-2}+ \cdots + c_ka_{n-k}, \quad n \ge k$$

$f(n) = 0$인 k계 선형 재귀식을 **k계 선형 동차 재귀식** ($k$ th-order linear homogeneous recurrence relation)이라고 한다.

<br/>

이를테면, 상수 $A,B$에 대해 식 $a_n = Aa_{n-1} + Ba_{n-2}, \, n \ge 2$와 같은 재귀식은 2계 선형 동차 재귀식(second-order linear homogeneout recurrence relation)이다.

<br/>

### <span style='background-color: #393E46; color: #F7F7F7'>&nbsp;&nbsp;&nbsp;예제 1.1.4&nbsp;&nbsp;&nbsp;</span>

세로X가로가 1X1인 노란색 사각형, 1X2인 파란색 사각형, 1X2인 빨간색 사각형이 각각 n개 있다. 이 사각형들로 1Xn 크기의 사각형을 만드는 방법의 수 $a_n$을 재귀함수로 나타내어라

### <span style='background-color: #C2B2B2; color: #F7F7F7'>&nbsp;&nbsp;&nbsp;풀이&nbsp;&nbsp;&nbsp;</span>

n = 1일 때 1X1인 노란색 사각형을 쓸 수 있다.($a_1 = 1$), n = 2일 때 노란색 2개 / 파란색 1개 / 빨간색 1개 총 세 가지 방법을 쓸 수 있다.($a_2 = 3$), 

이렇게 진행했을 때 처음 사각형이 노란색으로 시작하면, 나머지는 1X(n-1) 크기 사각형을 만들어야 하는 데, 그 방법의 수는 $a_{n-1}$개다. 반대로 1X2 크기(파란색 혹은 빨간색)으로 시작하면, 나머지는 1X(n-2) 크기 사각형을 만들어야 한다. 그 방법의 수는 $a_{n-2}$이다.

1. 초기조건: $a_1 = 1$, $a_2 = 3$

2. 재귀식: $a_n = a_{n-1} + 2a_{n-2}, \, n \ge 3$

위와 같은 2계 선형 동차 재귀식으로 표현된 재귀함수(점화수열)를 갖는다.

<br/>

### <span style='background-color: #393E46; color: #F7F7F7'>&nbsp;&nbsp;&nbsp;정의 1.1.2&nbsp;&nbsp;&nbsp;</span>

#### **n 팩토리얼**

1. $0! = 1$

2. $n! = n \cdot (n-1)!, \quad n \ge 1$

양의 정수 n에 대하여 위 초기조건과 재귀식을 만족하는 재귀 함수를 $n$**팩토리얼(factorial)**이라고 하고 $n!$로 쓴다.

<br/>

위 정의의 재귀식을 보면 $(n-1)!$의 계수가 **상수가 아닌** n이므로, 1계 선형 재귀식이 아니고 1계 재귀식(점화식)이다.

- 팩토리얼 n!의 크기

  - 간단한 부등식 이용: $n!$ 정의에 의해 $n \ge 4$인 경우에는 다음을 만족한다.

  $$ 2^n < n! < n^{n} $$

  - 스털링의 공식(Stirling's formula)를 사용하면 근사값을 구할 수 있다.

  $$n! \approx {\left( \frac{n}{e} \right)}^{n}\sqrt{2 \pi {n}}$$

### 1.1.2.1 재귀식의 해를 구하는 방법: 반복

재귀함수의 일반항 또는 일반식을 **재귀식의 해**(solution of recurrence relations)라고 한다. 해를 구하는 기법은 다양하게 있다.

### <span style='background-color: #393E46; color: #F7F7F7'>&nbsp;&nbsp;&nbsp;예제 1.1.5&nbsp;&nbsp;&nbsp;</span>

양의 정수 k에 대하여 재귀적으로 정의된 수열의 일반항을 구하라

- (1) $m_k = 2m_{k-1} + 1, \, k \ge 2, \, m_1 = 1$

- (2) $a_n = na_{n-1} + 1, \, n \ge 1, \, a_0 = 0$

### <span style='background-color: #C2B2B2; color: #F7F7F7'>&nbsp;&nbsp;&nbsp;풀이&nbsp;&nbsp;&nbsp;</span>

(1)번 풀이

$m_1 = 1$,

$m_2 = 2m_1 + 1 = 2 \cdot 1 + 1$,

$m_3 = 2m_2 + 1 = 2(2+1)+1 = 2^2 + 2^1 + 1$,

$m_4 = 2m_3 + 1 = 2(2^2 + 2^1 + 1) + = 2^3 + 2^2 + 2^1 + 1$

$\quad \vdots$

$m_k = 2^{k-1} + 2^{k-2} + \cdots + + 2^2 + 2^1 + 1  = {2^k - 1 \over 2 -1 } = 2^k - 1, \quad k \ge 1$

따라서 일반항은 $2^k - 1, \, k \ge 1$이다.

<br/>

(2)번 풀이

$a_n = n \cdot a_{n-1} + 1$

$\quad \; = n((n-1) \cdot a_{n-2} + 1) + 1$

$\quad \; = n(n-1) \cdot a_{n-2} + n + 1$

$\quad \; = n(n-1)(n-2) \cdot a_{n-3} + n(n-1) + n +1$

$\qquad \vdots$

$\quad \; = {n! \over (n-k)!} \cdot a_{n-k} + {\left( {n! \over (n - (k - 1))!} + \cdots + {n! \over n!} \right)}$

$\quad \; = {n! \over (0)!} \cdot a_{0} + {\left( {n! \over 1!} + {n! \over 2!} +  \cdots + {n! \over   (n-1)!} + {n! \over n!} \right)}$

$\quad \; = \sum_{k=1}^{n}{n! \over k!}$

<br/>

### 1.1.2.2 k계 선형 동차 재귀식의 해

2계 이상의 재귀식 같은 경우에는 대체로 패턴을 구하기 쉽지 않아서 다른 기법이 필요하다. 

$$a_n = c_1a_{n-1} + c_2a_{n-2} + \cdots + c_ka_{n-k}, \; n \ge k$$

공비가 $t(\ne 0)$인 등비수열 $\{t^n: n = 0, 1, .... \}$이 위와 같은 k계 선형 동차 방정식을 만족하면, 이 재귀식에 $a_i = t^i$를 대입하면

$$t^n = c_1t^{n-1} + c_2t^{n-2} + \cdots + c_ka^{n-k}, \; n \ge k$$

위와 같이 식의 형태를 바꿀 수 있다. 위 식의 양변을 $t^{n-k}$로 나누면

$$t^k = c_1t^{k-1} + c_2t^{k-2} + \cdots + c_k$$

즉,

$$t^k - c_1t^{k-1} - c_2t^{k-2} - \cdots - c_k = 0, \; c_k = 0$$

이 되어 공비 $t(\ne 0)$는 k차 방정식의 해가 된다. (반대로 공비 $t(\ne 0)$인 k차 방정식이 주어졌을 때 양변에 $t^{n-k}$를 곱해서 k계 선형 동차 방정식 형태로 만들 수 있다.)

k계 선형 동차 재귀식에서 도출한 이러한 k차 방정식을 **특성방정식(characterisic polynomial)**라고 한다.

> 다시 말해 이 특성방정식의 해 $t(\ne 0)$가 공비인 등비수열 $\{t^n: n = 0, 1, .... \}$은 k계 선형 동차 재귀식을 만족하는 필요충분조건이다.

예를 들어 아래 2차 선형 동차 재귀식이 있다면, (A, B는 상수)

$$ a_n = Aa_{n-1} + Ba_{n-2}, \; n \ge 2 $$ 

이 2차 선형 동차 재귀식의 특성방정식

$$ t^2 - At - B $$

의 서로 다른 해를 $u, w$라고 하면 두 수열 $\{u^n\}$, $\{w^n\}$이 선형 동차 재귀식을 만족할 뿐만 아니라, 두 수열의 일차결합으로 표현된 수열 $\{Cu^n + Dw^n\}$도 같은 선형동차식을 만족하게 된다.(linear 특성상)

그러므로 수열 $\{Cu^n + Dw^n\}$도 초기조건만 만족하면, 재귀수열 $a_n$과 같은 수열처럼 분석할 수 있다. 일반적으로 2계 선형 동차 재귀식을 포함하는 재귀수열은 2개의 초기조건이 주어지므로, 계수 C와 D를 결정할 수 있다.

한편 특성방정식 $t^2 - At - B$가 $(t-u)^2$ 형태로 중근 $u$를 갖는다면($t^2 - 2ut + u^2$), 수열 ${u^n}$이 선형 동차 재귀식을 만족할 뿐만 아니라, $\{nu^n\}$도 같은 선형 동차 재귀식을 만족하게 된다.

$$A(n-1)u^{n-1} + B(n-2)u^{n-2}$$

$$\qquad = 2u(n-1)u^{n-1} - u^2(n-2)u^{n-2}$$

$$\qquad \qquad \quad \; = 2(n-1)u^n - (n-2)u^n = nu^n \; (n \ge 2)$$

비슷하게 증명하면 수열 $\{Cu^n + Dnu^n \}$도 재귀식을 만족하고, 초기조건을 만족하면 상수 C, D를 찾으면 재귀수열을 만족하는 수열의 일반항은 $a_n = Cu^n + Dnu^n$과 같다.

<br/>

### <span style='background-color: #FB2575; color: #F7F7F7'>&nbsp;&nbsp;&nbsp;정리 1.1.1&nbsp;&nbsp;&nbsp;</span>

2계 선형 동차 재귀식 $a_n = A a_{n-1} + B a_{n-2}, \; n \ge 2$로 정의된 수열의 일반항 $a_n$은 다음과 같다.

1. 재귀식의 특성방정식 $t^2 - At - B = 0$이 서로 다른 해 $u, w$를 갖는다면 수열의 일반항은 아래와 같으며, 상수 C, D는 초기조건에 의해 결정된다.

$$a_n = Cu^n + Dw^n$$

2. 재귀식의 특성방정식 $t^2 - At - B = 0$이 중근 $u$를 갖는다면 수열의 일반항은 아래와 같으며, 상수 C, D는 초기조건에 의해 결정된다.

$$a_n = Cu^n + Dnu^n$$

<br/>

### <span style='background-color: #393E46; color: #F7F7F7'>&nbsp;&nbsp;&nbsp;예제 1.1.7&nbsp;&nbsp;&nbsp;</span>

아래 재귀수열의 일반항 $a_n$을 n으로 나타내어라.

$a_n = a_{n-1} + 2a_{n-2}, \, n \ge 3$, $a_1 = 1$, $a_2 = 3$

### <span style='background-color: #C2B2B2; color: #F7F7F7'>&nbsp;&nbsp;&nbsp;풀이&nbsp;&nbsp;&nbsp;</span>

재귀식의 특성방정식은 아래와 같다.

$$ t^2 - t -2 = 0 $$

이 재귀방정식을 풀면 해는 $t = 2, \; -1$이므로 일반항은

$$ a_n = C2^n + D(-1)^n $$

형태이다. 초기조건에 따라 $C= {2 \over 3}, D = {1 \over 3}$을 얻을 수 있다. 따라서 일반항은 아래와 같다.

$$ a_n = {2 \over 3} \cdot 2^n + {1 \over 3} (-1)^n, \; n \ge 1 $$

<br/>

k계 선형 동차 재귀식도 이와 유사하게 확장하면 수열의 일반항을 구할 수 있다.

### <span style='background-color: #393E46; color: #F7F7F7'>&nbsp;&nbsp;&nbsp;예제 1.1.8&nbsp;&nbsp;&nbsp;</span>

아래 재귀함수를 만족하는 수열 $\{x_n\}$의 일반항을 구하여라.

$\begin{cases}
x_0 = 0, x_1 = 2, x_2 = 6 \\ 
x_n = 4x_{n-1} - x_{n-2} - 6x_{n-3}, \; (n \ge 3) \\
\end{cases}$

### <span style='background-color: #C2B2B2; color: #F7F7F7'>&nbsp;&nbsp;&nbsp;풀이&nbsp;&nbsp;&nbsp;</span>

재귀식의 특성방정식

$$ t^3 - 4t^2 + t + 6 = 0$$

의 해를 구하면 $t = 2, 3, -1$이다. 따라서 일반항은 아래와 같은 형태다.

$$x_n = C2^n + D3^n + E(-1)^n$$

초기조건을 대입하면 $C = -{2 \over 3}, D = 1, E = - {1 \over 3}$을 얻을 수 있다. 따라서 일반항은

$$ x_n = -{2 \over 3} \cdot 2^n + 3^n - {1 \over 3} (-1)^n, \; n \ge 0 $$

이다.

<br/>

---

<br/>

