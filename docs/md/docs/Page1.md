# 컴파일 상수와 런타임 상수 (+constexpr)	
<hr>
c++에서는 두가지 상수가 존재한다 

1. 컴파일 시간에 알 수 있는 상수 - 컴파일 상수

2. 컴파일 시간에 알 수 없는 상수 - 런타임 상수(실행시간에 알 수 있는 실행시간 상수)

예시를 들자면 
	const int size = 7;
	int arr[size]; 
	c++에선 맥락에 따라 const 가 변하게 되는데 위와 같은 경우
	컴파일 상수로 기능하여 오류없이 코드가 동작한다 하지만
	int num = 7;
	const int size = num;
	int arr[size];
	이와 같은 경우에는 const 가 런타임 상수로 기능하여 
	동작이 불가능 하게 된다
다음과 같은 경우를 방지하기 위해 c++에는 constexpr 가 존재한다
constexpr 는 컴파일 타임 상수이다 const에 컴파일 타임 상수임을 기재한 것
	constexpr int const(123); 정상 동작
<hr>
	int number;
	cin >> number;
	constexpr int const_test(number); 는 불가능
<br>

<br>


> :ToCPrevNext