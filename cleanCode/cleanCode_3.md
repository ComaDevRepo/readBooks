# Clean Code

## Chapter 3 함수

* 프로그램의 가장 기본적인 단위가 함수이다.
* 작게 만들어라
	* 함수를 만드는 첫번째 규칙은 '작게'다.
	* 두번째는 '더 작게'이다.
	* if/else , while등에 들어가는 블록은 한 줄이어야한다.
	* 함수가 중첩구조가 생길만큼 커져서는 안된다.
	* 함수에서 들여쓰기 수준은 1단이나 2단을 넘어서면 안된다.
* 한가지만 해라
	* 함수는 한가지만 해야한다.
	* 함수가 지정된 함수 이름 아래에서 추상화 수준이 하나인 단계만 수행한다면 그 함수는 한가지 작업만 한다.
	* 함수를 만드는 이유는 큰 개념을 다음 추상화 수준에서 여러 단계로 나눠 수행하기 위해서이다.
	* 함수의 의미있는 이름으로 다른 함수를 추출할 수 있다면 그 함수는 여러 가지 작업을 하는 함수이다.
* 함수 당 추상화 수준은 하나로
	* 함수가 확실히 한 가지 작업만 하려면 함수 내 모든 문장이 동일한 추상화 수준에 있어야 한다.
	* 한 함수 내에서 추상화 수준을 섞으면 코드를 읽는 사람이 햇갈린다.
* 위에서 아래로 코드 읽기 : 내려가기 규칙
	* 코드는 위에서 아래로 이야기 처럼 읽혀야 좋다.
	* 한 함수 다음에는 추상화 수준이 한 단계 낮은 함수가 온다.
	* 일련의 TO 문단을 읽듯이 프로그램이 읽혀야 한다는 의미.
* switch 문
* 서술적인 이름을 사용하라
	* 길고 서술적인 이름이 짧고 어려운 이름보다 낫다.
	* 이름을 붙일때는 일관성이 있어야 한다.
	* 모듈 내에서 함수 이름은 같은 문구,명사,동사를 사용한다.
	* 문체가 비슷하면 이야기를 순차적으로 풀어가기 쉬워진다.
* 함수 인수
	* 함수에서 이상적인 인수 개수는 0개이다. (4개 이상은 사용하면 안된다.)
	* 인수는 개념을 이해하기 어렵게 만든다.
	* 출력 인수는 입력 인수보다 이해하기 어렵다.
* 많이 쓰는 단항 형식
	* 함수에 인수를 1개 넘기는 이유
		* 인수에 질문을 던지는 경우
		* 인수를 뭔가로 변환해 결과를 반환하는 경우
* 플래그 인수
	* 함수가 여러 가지를 처리한다고 대놓고 공표하는 샘이여서 추하다.
* 이항 함수
	* 인수가 2개인 함수는 1개인 함수보다 이해하기 어렵다.
* 삼항 함수
	* 인수가 3개인 함수는 인수가 2개인 함수보다 훨씬 더 이해하기 어렵다.
	* 삼항 함수를 만들 때는 신중하라.
* 인수 객체
```
Circle makeCircle(double x, double y, double radus);
Circle makeCircle(Point center, double radus);
```
	* 변수를 묶어서 넘기려면 이름을 붙여야 하므로 결국 개념을 표현하게 된다.

* 인수 목록
* 동사와 키워드
	* 단항 함수는 함수와 인수가 동사/명사 쌍을 이뤄야 한다.
* 부수 효과를 일으키지 마라
	* 함수에서 한가지 일만 하겠다고 약속하고 남몰래 여러가지를 하게하지 마라.
* 출력 인수
	* 일반적으로 출력 인수는 피해야 한다.
	* 함수에서 뭔가의 상태를 변경해야 한다면 함수가 속하는 객체의 상태를 변경하는 방법을 택한다.
* 명령과 조회를 분리하라.
	* 함수는 뭔가를 수행하거나 뭔가에 답하거나 둘 중 하나만 해야 한다.
* 오류 코드보다 예외를 사용하라.
	* 명령 함수에서 오류 코드를 반환하는 방식은 명령/조회 분리 규칙을 미묘하게 위반한다.
* try/catch 블록 뽑아내기
	* 별도의 함수로 뽑아내는 편이 낫다.
* 오류 처리도 한 가지 작업이다.
* 반복하지 마라
	* 중복은 문제다
	* 코드 길이가 늘어나고, 알고리즘이 변하면 중복된곳을 모두 고쳐야 한다.
	* 중복은 소프트웨어에서 모든 악의 근원이다.
* 구조적 프로그래밍
	* 함수가 아주 클때만 상당한 이익을 제공한다.
* 함수를 어떻게 작성하나?
	* 먼저 생각을 기록한 후 읽기 좋게 다듬는다.

함수는  그 언어에서 동사며, 클래스는 명사다.
프로그래밍의 기술은 언제나 언어 설계의 기술이다.