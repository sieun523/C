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
