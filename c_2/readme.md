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
```
```c
#define _CRT-SECURE_NO_WARNINGS 
#include <stdio.h>

int main(void)
{
    int x;
    int y;
    int sum;

    printf("첫번째 숫자를 입력하시오:");
    scanf("%d", &x);

    printf("두번째 숫자를 입력하시오:");
    scanf("%d", &y);

    sum = x + y;
    printf("두수의 합:%d", sum);

    return 0;
}
```
```c
#define _CRT-SECURE_NO_WARNINGS 
#include <stdio.h>

int main(void)
{
   float radius; //원의 반지름
   float area;  // 면적

   printf("반지름을 입력하시오:");
   scanf("%f", &radius);

   area = 3.14 * radius * radius;
   printf("원의 면적:%f", area);
   
    return 0;
}
```
```c
#define _CRT-SECURE_NO_WARNINGS 
#include <stdio.h>

int main(void)
{
    double rate; //원 / 달러 환율
    double usd; //달러화
    int krw; // 원화는 정수형 변수로 선언

    printf("환율을 입력하시오:");
    scanf("%lf", &rate);

    printf("원화 금액을 입력하시오:");
    scanf("%d", &krw);

    usd = krw / rate;
    printf("원화 %d원은 %lf달러 입니다.", krw, usd);

    return 0;
}
```
```c
#define _CRT_SECURE_NO_WARNINGS 
#include <stdio.h>

int main(void)
{
    double num1, num2, num3;
    double sum, avg;

    printf("3개의 실수를 입력하시오:");
    scanf("%lf %lf %lf", &num1, &num2, &num3); //3개의 실수 입력

    sum = num1 + num2 + num3;
    printf("합계=%.2lf\n", sum);  //소수점 이하를 2자리로 표시

    avg = sum / 3;
    printf("평균=%.2lf\n", avg);  //소수점 이하를 2자리로 표시


    return 0;
}
```
```c
#define _CRT_SECURE_NO_WARNINGS 
#include <stdio.h>

int main(void)
{
    double w, h;
    double area, perimeter;

    w = 10.0;
    h = 5.0;
    area = w * h;
    perimeter = 2 * (w+h);

    printf("사각형의 넓이:%lf\n", area);
    printf("사각형의 둘레:%lf\n", perimeter);

    return 0;
}
```
