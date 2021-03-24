# **KS동아리 과제**
'**변수와 상수**\
*라이브러리 불러오기*</br>
C에서는 #include 명령어를 이용해 다양한 라이브러리를 불러올 수 있다.\
집을 지으려면 망치와 같은 도구가 필요하듯이 stdio.h는 여러 기본적인 기능을 담고 있다.

*메인함수*\
C에서는 다양한 함수가 사용될 수 있으나 프로그램은 항상 메인(main)함수로부터 시작된다.\
함수는 반환값(Return Value)이 없을 수도 있으나 메인 함수에서는 항상 0을 반환하는 것이 일반적이다.

C에서는 특정한 문자들을 출력하기 위해 printf()함수를 사용 
printf()는 stdio.h 헤더 파일에 포함되어있음
C에서는 하나의 명령어가 끝났음을 알리기 위해 세미콜론(;)을 붙임

명령 프롬프트에서 pause 명령어는 키보드를 입력하기 전까지 대기하는 기능을 수행함  
printf("HI");  
system("pause")

*변수와 상수의 개념*  
변수(Variable)는 변할 수 있는 데이터  
상수(Constant)는 변하지 않는 데이터

*변수의 선언*\
변수를 선언할 때는 자료형과 변수명을 입력, 원하는 경우 초기값을 적용할 수 있음
가장 많이 사용되는 변수는 정수형 변수  
int a;  
int a = 4;

*변수의 초기화와 쓰레기값*  
초기화 되지 않은 변수는 쓰레기 값이 들어감  
Visual Studio는 기본적으로 초기화 되지 않는 변수를 감지하고 오류를 출력함\
#include<stdio.h>

int main(void) {  
	int a;  
	printf("숫자는 #d.\n", a);  
	system("pause");  
	return 0;  
}

정적 변수로 선언된 것은 기본적으로 0으로 값이 초기화 됨  
정적 변수가 아닌 수를 0으로 초기화 하려면 값을 일일이 넣어주어야함

*기본적인 자료형*  
int : 일반적인 정수형을 표현  
long long : 숫자가 긴 정수형을 표현  
double : 일반적인 실수형을 표현  
string : 문자열을 표현  
bool : 참/거짓을 표현   
char : 한 문자를 표현  

*예약어와 식별자*  
식별자란 변수나 함수 등의 고유한 이름을 지정할 때 사용\
이때 C문법으로 정해진 예약어는 식별자로 사용할 수 없음  
string, for, void, bool, if, while, char, return, double

*기본입출력*  
scanf()입력  
C에서 특정한 변수에 값을 넣기 위해 scanf()를 사용함  
#include <stdio.h>\
int main(void) {\
	int a;\
	scanf("%d", &a);\
	printf("입력한 숫자는 %d입니다.\n“, a)\
	system("pause");\
	return0;\
}

Visual Studio는 기본적으로 취약한 함수를 사용할 수 없도록 제한함  
따라서 _CRT_SECURE_NO_WARNINGS를 적용함  
Visual Studio를 제외한 대부분의 IDE에서는 scanf()를 사용해도 컴파일이 진행됨  
#define _CRT_SECURE_NO_WARNINGS  
#include <stdio.h>  
int main(void) {  
	int a;  
	scanf("%d", &a);  
	printf("입력한 숫자는 %d입니다.\n“, a)  
	system("pause");  
	return0;  
}  
scanf()를 이용할 때 &를 이용하는 이유는 &는 특정한 변수의 주소를 의미함  
실제 컴퓨터는 특정한 메모리 주소에 접근하여 데이터를 수정하므로 &를 이용하는것임  
그렇다면 메모리 주소에 얼마만큼의 크기로 데이터를 쓸지 결정해야됨

*형식지정자*  
int(4byte), %d, 정수  
long long(8byte), %lld, 정수  
double(8byte), 입력시 %lf, 출력시 %f, 실수  
float(4byte), %f, 실수  
string(제한없음), %s, 문자열데이터  
char(1byte), %c, 문자데이터  
'