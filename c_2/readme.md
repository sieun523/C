# 2023-03-09 2주차 수업

```c
// 정수 간의 가감승제를 계산하는 프로그램
#include <stdio.h>

int main(void)
{
    int x;   //첫 번째 정수를 저장할 변수
    int y;   //두 번째 정수를 저장할 변수
    int sum, diff, mul, div;  // 두 정수 간의 연산의 결과를 저장하는 변수

    x = 20;   // 변수 x에 2을 저장
    y = 10;   // 변수 y에 10을 저장

    sum = x + y;  // 변수 sum에 (x+y)의 결과를 저장
    diff = x - y;  // 변수 diff에 (x-y)의 결과를 저장
    mul = x * y;   // 변수 mul에 (x*y)의 결과를 저장
    div = x / y;   // 변수 div에 (x/y)의 결과를 저장

    printf("두수의 합: %d\n", sum);  //변수 sum의 값을 화면에 출력
    printf("두수의 차: %d\n", diff); //변수 diff의 값을 화면에 출력
    printf("두수의 곱: %d\n", mul);  //변수 mul의 값을 화면에 출력
    printf("두수의 몫: %d\n", div);  //변수 div의 값을 화면에 출력

    return 0;

}
```
```c
#define _CRT-SECURE_NO_WARNINGS //scanf()에 오류가 발생하면 소스 파일의 처음에 정의해준다
#include <stdio.h>

int main(void)
{
    int x;
    printf("정수를 입력하시오:");
    scanf("%d", &x);  //형식지정자와 변수의 주소 입력
    printf("입력된 정수 = %d\n", x);
    return 0;

}
