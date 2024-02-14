## 一些C语言要注意的问题

### 1.`include`语句
 - 一定要注意, 引入的是`<stdio.h>`, 不是别的东西!
 - 当你需要求绝对值、平方根、次方时， 一定要用`#include <math.h>`。

### 2. `main()`函数
 - **是main**,不是mian,不是mina,不是mnai!!!!!

### 3.`if`语句
 - `if`语句的格式是`if(条件表达式) { 语句 }`,不管语句有多少条,都用大括号括起来.~~老师曾经是说过,语句只有一条时可以不用括号~~.但为了方便查找错误,**请带上括号**.
 - 条件语句中判断是否相等是**两个等号**!

### 4.`for`循环
 - 当一个程序有多个for循环时,可以这样写:
 ```
 for(int i=0; i< balabala; i++){
    for(int j=0; j< balabala; j++){
        balabala;//这里是第一个for循环的语句
    }
 }

 //第二套for循环可以继续用i,j,两个for循环的循环变量是不会相互影响的 

 for(int i=0; i< balabala; i++){
    for(int j=0; j< balabala; j++){
        balabala;//这里是第二个for循环的语句
    }
 }
```

 - 如果脑子不够用,循环变量从1开始算也是可以的,
   - 上面的示例从0开始,循环到小于balabala就行了,这个时候i=balabala-1,循环了i-0+1=balabala次.
    - 当然,从1开始算就要循环到小于等于balabala,这个时候i=balabala,循环了i-1+1=balabala次.

### 5. 变量精度问题
- 如果题上没有要求,我们这个阶段默认都是整数,用`int`就行了. 
- 需要用到小数的时候,如果题目上没有明确要求,用`double`.
- 这些情况,即使参与运算的都是整数,也要用double:
  - 使用pow函数时
  - 使用sqrt函数时

### 6. 请不要把你的代码写得像一坨勾史
给你两端代码,这两段代码中都有明显的错误,请查找一下:

提示:两端代码错误一样.

 ```clike
#include <stdio.h>
int main(){
int count, min, num;
scanf("%d", &count);
scanf("%d", &num);
min = num;
for (int i = 0; i < count - 1; i++)
{scanf("%d", num);
if (min > num)
min = num;}}
printf("min = %d", min);
return 0;}
 ```


 ```clike
#include <stdio.h>
int main()
{
    int count, min, num;
    scanf("%d", &count);
    scanf("%d", &num);
    min = num;
    for (int i = 0; i < count - 1; i++)
    {
        scanf("%d", &num);
        if (min > num)
        
            min = num;
        }
    }
    printf("min = %d", min);
    return 0;
}
 ```
### 7.其他一些小问题
 - 分号不要丢 分号不要丢 分号不要丢 
 - 一定要注意返回的内容和函数声明的返回内容要对上,比如

```clike
int fun(){//这里声明了函数要返回一个int类型.
    int i;
    return i; //这里返回的i,一定要声明为int类型,否则编译会出错.
}
```

### 8.第6条答案
if语句的大括号少了一半,左大括号丢了.两部分代码排错哪个更简单一点更好找一点?相信你自己心中已经有了答案!