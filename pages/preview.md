# 可不是游戏机哦！

接下来我们来学习一下`switch`语句。在日常生活中，我们可以找到很多“switch”。像灯的开关，电脑的开关，手机的电源键等等。C语言中的switch，更像是一个风扇调速器。它可以有很多个选项！

我们和往常一样，先来一段代码：

```clike
#include <stdio.h>

int main(){
    int choice;
    scanf("%d",&choice);
    switch (choice) 
    {
    case 1:
        printf("A");
        break;
    case 2:
        printf("B");
        break;
    case 3:
        printf("C");
        break;
    case 4:
        printf("D");
        break;
    default:
        printf("Unknown Choice");
        break;
    }
}
```

前面已经讲过的内容就不在赘述了，我们一起来分析一下`switch`语句。

## `switch()`

这里是`switch`语句的开头，和`if`不同，`switch`的括号里面**不装表达式**哦！里面只需要装**一个变量名**。比如这里装的就是通过`scanf`获得的`choice`;

## `case _ :`

`case`这里就是对情况的列举啦，通常只有所有情况是可以全部写出时才采用switch语句，也就是说，要在大括号里把所有情况全部罗列出来！