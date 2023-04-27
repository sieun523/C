# 2023-3-16 3주차
```c
#include <stdio.h>

int main(void)
{
    int x;

    printf("변수 x의 크기:%d\n", sizeof(x));
    printf("char형의 크기:%d\n", sizeof(char));
    printf("int형의 크기:%d\n", sizeof(int));
    printf("short형의 크기:%d\n", sizeof(short));
    printf("long형의 크기:%d\n", sizeof(long));
    printf("float형의 크기:%d\n", sizeof(float));
    printf("double형의 크기:%d\n", sizeof(double));

    return 0;
}
```
```c
#include <stdio.h>
#include <limits.h> //각 자료형의 최대값과 최소값은 여기에 정의되어 있다.

int main(void)
{
    short s_money =SHRT_MAX; //최대값으로 초기화한다. 32767
    unsigned short u_money = USHRT_MAX; //최대값으로 초기화한다. 65535

    s_money = s_money + 1;     //오버플로우 발생
    printf("s_money = %d\n", s_money);

    u_money = u_money +1;
    printf("u_money = %d\n", u_money);
    return 0;
}
```
```c
#include <stdio.h>

int main(void)
{
    int x = 10;  //10은 10진수이고 int형이고 값은 십진수로 10이다.
    int y = 010; //010은 8진수이고 int형이고 값은 십진수로 8이다.
    int z = 0x10;  //0x10은 16진수이고 int형이고 값은 십진수로 16이다.

    printf("x = %d\n", x);
    printf("y = %d\n", y);
    printf("z = %d\n", z);

    return 0;
}
```
```c
#include <stdio.h>
#define TAX_RATE 0.2  //기호상수

int main(void)
{
    const int MONTHS = 12;  //기호상수
    int m_salary, y_salary; //변수 선언

    printf("월급을 입력하시오:"); 
    scanf("%d", &m_salary);

    y_salary = MONTHS * m_salary; //순수입 계산
    printf("연봉은 %d입니다.", y_salary);
    printf("세금은 %f입니다.", y_salary * TAX_RATE);

    return 0;
}
```
```c
#include <stdio.h>

int main(void)
{
    int x = 3;
    int y = -3; //음수가 2의 보수로 표현되는지를 알아보자

    printf("x = %08x\n", x); //8자리의 16진수로 출력한다.
    printf("y = %08x\n", y); //8자리의 16진수로 출력한다.
    printf("x+y = %08x\n", x+y);  //8자리의 16진수로 출력한다.

    return 0;
}
```
```c
#include <stdio.h> /*부동 소수점 자료형의 크기 계산*/

int main(void)
{
    float x = 1.234567890123456789;
    double y = 1.234567890123456789;

    printf("float의 크기 = %d\n", sizeof(float));
    printf("double의 크기 = %d\n", sizeof(double));

    printf("x = %30.25f\n", x);
    printf("y = %30.25f\n", y);
    return 0;
}
```
```c
#include <stdio.h> /*부동 소수점 자료형의 크기 계산*/

int main(void)
{
    float x = 1.23456e-38;
    float y = 1.23456e-40;
    float z = 1.23456e-46; //숫자가 작아서 언더플로우 발생

    printf("x = %e\n",x);
    printf("x = %e\n",y);
    printf("x = %e\n",z);

    return 0;
}
```
