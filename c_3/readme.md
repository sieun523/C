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
```c
#include <stdio.h>      /*부동소수점 사용시 주의 사항*/

int main(void)
{
    float value = 0.1;        /*이진법으로는 정확하게 나타낼 수 없는 값들이 있기 때문이다. 0.1도 
                              그 중의 하나이다. */

    printf("%.20f\n", value); // %.20는 소수점 이하를 20자리로 출력

    return 0;
}
```
```c
#include <stdio.h>      /*부동소수점 사용시 주의 사항*/

int main(void)
{
    double x;

    x = (1.0e20 + 5.0)-1.0e20; //부동소수점 연산에서는 오차가 발생한다. 5.0이 아니라 0으로 계산된다.
    printf("%f\n", x);
    return 0;
}
```
```c
#include <stdio.h>

int main(void)
{
    char code1 = 'A';
    char code2 = '65';

    printf("code1 = %c\n", code1);
    printf("code2 = %c\n", code2);
    return 0;
}
```
```c
#include <stdio.h>
int main(void)
{
    int id, pass;

    printf("아이드와 패스워드를 4개의 숫자로 입력하시오:\n");

    printf("id:____\b\b\b\b");
    scanf("%d", &id);

    printf("pass:____\b\b\b\b");
    scanf("%d", &pass);
    printf("\a입력된 아이디는 \"%d\"이고 패스워드는 \"%d\"입니다.", id, pass);

    return 0;

}
```
```c
#include <stdio.h>
int main(void)
{
    char code = 'A';
    printf("%d %d %d\n", code, code+1, code+2); //65 66 67이 출력된다.
    printf("%c %c %c\n", code, code+1, code+2); // A B C가 출력된다
    return 0;

}
``` 
```c
#include <stdio.h>
int main(void)
{
    int x, y, z, sum;
    sum = 0; //변수는 사용하기 전에 반드시 초기화 시켜야 함!! 아니면 에러

    printf("3개의 정수를 입력하세요(x,y,z):");
    scanf("%d %d %d", &x, &y, &z);
    sum += x;
    sum += y;
    sum += z;
    printf("3개의 정수의 합은 %d\n", sum);
    return 0;

}
``` 
```c
#include <stdio.h>
int main(void)
{
    double light_speed = 300000; //빛의 속도 저장하는 변수    //초기화
    double distance = 149600000; //태양과 지구 사이 거리 저장하는 변수
        
    double time;  //시간을 나타내는 변수

    time = distance / light_speed;  //거리를 빛의 속도로 나눈다
    time = time / 60.0;  //초를 분으로 변환한다

    printf("빛의 속도는 %fkm/s \n", light_speed); //빛의 속도 출력
    printf("태양과 지구와의 거리 %fkm\n", distance); //거리 출력
    printf("도달 시간은 %f초 \n", time); //시간을 출력
    
    return 0;

}
```
