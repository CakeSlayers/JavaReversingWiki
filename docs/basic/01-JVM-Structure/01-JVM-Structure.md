# JVM结构

> 简单介绍一下，这部分知识暂时不用钻研

先说一个奇葩的事，其实JVM自己一点都不会JAVA语言，它只会自己的指令码即Java字节码(Java bytecode)。

所以Java程序的流程是：

Java源代码被javac编译以后变成了Java字节码，然后放入JVM才能被JVM识别并运行![Java运行流程](第一章img/Java运行流程.png)





## 线程(Threads)：

Java的框架是并行的，这意味着不同的计算可以用多个线程在同一时间运行。

当一个新的JVM进程启动时，创建的第一个新线程即主线程(main thread)。

主线程创建后，在static main(String[] args)中的代码就开始在主线程中运行。





## 帧栈(Stack/Stackframe)与帧(Frames)：

每个Java线程都拥有一个帧栈来进行方法调用和返回，帧栈相当于帧的容器，用来控制方法调用和返回。JVM会为方法创建帧，当方法`return`时，对应的方法帧就会被销毁。

![JVM结构](第一章img/JVM结构.png)





## 帧(Frames)的结构（之后细讲）：

帧又称方法帧，用来处理每个方法里的内容。帧包含两个主要部分：局部变量表、操作栈





引用&参考：https://www.overops.com/blog/jvm-architecture-101-get-to-know-your-virtual-machine/

