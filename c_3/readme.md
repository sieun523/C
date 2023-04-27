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
