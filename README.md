# Hello

欢迎来到C语言魔法书，此网站还在更新当中，有任何问题请及时反馈

请点击三条杠进入目录

<font color=#42b983>[点击此处传送至作业解析](/pages/作业.md)</font>

<font color=#42b983>[如果你不知道今天吃什么，点这里抽一个吃吧:)](https://dragonte6967.gitee.io/pages/吃什么.html)</font>

# CHANGE LOGS

<font color= #42b983>

 - 2023/10/16 更改代码字体为`JetBrains Mono`，网站字体为`Harmony Sans`

 - 2023/10/16 转移了托管服务商，网络连接不稳定已修复

 - 2023/10/15 更新了两篇文档，优化了相关入口，网络连接不稳定尚未修复

 
</font>


# 开始之前

在开始阅读之前，你应该了解到：

## 不能像学外语一样学编程语言

 C语言不是自然语言，也不是人与人之间交流的工具，它只是人和机器沟通的桥梁，**请不要**用学习外语的方法学习C语言。**学好C语言的第一步就是把笔和笔记本丢一边**，然后打开电脑，~原神，启动！~

## 要把代码写的更加美观

 虽然C语言不是人与人之间沟通的工具，但它同时要满足**人和机器都能读懂**，这就要求我们要把代码写的尽量美观易读一些。

 ## 示范一下

 <!-- tabs:start -->

 ### **不易读**

```clike
# include <stdio.h>
int main()
{
int a,b;
scanf("%d%d",&a,&b);
printf("%d + %d = %d\n%d - %d = %d\n%d * %d = %d\n%d / %d = %d",a,b,a+b,a,b,a-b,a,b,a*b,a,b,a/b);
return 0;
}
```

### **依托答辩**

 ```clike
# include <stdio.h>
int main(){int a,b;scanf("%d%d",&a,&b);printf("%d + %d = %d\n%d - %d = %d\n%d * %d = %d\n%d / %d = %d",a,b,a+b,a,b,a-b,a,b,a*b,a,b,a/b);return 0;}
 ```

 ### **易读**

```clike
# include <stdio.h>

int main(){
    int a,b;
    scanf("%d%d",&a,&b);
    printf("%d + %d = %d\n%d - %d = %d\n%d * %d = %d\n%d / %d = %d",
            a, b, a + b,
            a, b, a - b,
            a, b, a * b,
            a, b, a / b);
    return 0;
}
```

 <!-- tabs:end -->

很容易发现，第三组中，  `include`语句和方法语句之间插入了**空行**，变量声明中变量名、赋值、变量值之间都添加了一个**空格**，大括号中的函数体也进行了**缩进**。

如果不做上述措施，会显得很挤，当代码量增加，出现`for`循环等循环体时，会因读错层级导致读错，也为代码排查带来不少麻烦。

~当然，如果能够保证代码只有自己查看，可以随心所欲的写。~

## 关于注释

~如果能够保证代码只有自己查看，可以随心所欲的写，甚至不写。~ 代码量达到一定程度时，不写注释会给bug检查带来极大的麻烦。

## 自己动手，丰衣足食！

虽然这里提供了一些题目的一些解题思路，但是我相信手打代码对于大家来说都是**轻而易举**的事情。一般来说，自己手打一遍印象更深哦！当然，这里的代码并没有设置“不可复制”模式，~方便大家复制下来运行，一起查找其中的bug。~

 