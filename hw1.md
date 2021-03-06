## 填空题

---
* 当前常见的操作系统主要用C,C++,ASM编程语言编写。
* "Operating system"这个单词起源于Operator。
* 在计算机系统中，控制和管理各种资源、有效地组织多道程序运行的系统软件称作操作系统。
* 允许多用户将若干个作业提交给计算机系统集中处理的操作系统称为批处理操作系统
* 你了解的当前世界上使用最多的32bit CPU是ARM，其上运行最多的操作系统是Android。
* 应用程序通过系统调用接口获得操作系统的服务。
* 现代操作系统的特征包括并行性，虚拟性，异步性（不确定性）、共享性和持久性。
* 操作系统内核的架构包括宏内核（单体内核,monolithic kernel），微内核(microkernel)，外核（exokernel）。


---
## 问答题

- 请总结你认为操作系统应该具有的特征有什么？并对其特征进行简要阐述。

从总体上看，操作系统具有五个方面的特征：虚拟性、并发性、异步性、共享性和持久性。

并发是指说我们在操作系统当中有多个正在运行的应用程序,那么它需要操作系统管理和调度.就是如果多个应用程序交替运行,我需要知道当前每一个应用,都执行到什么位置,当前正在执行的是哪个应用.如果说应用之间有切换,那切换到下一个应用的时候,它上次执行到什么位置,那这次我从什么地方开始,当时的状态是什么样子,都用操作系统来维护.

共享是指说我们多个应用并发运行的时候宏观上要体现出它们同时在访问资源的情况,微观上要实现它们的互斥访问.比如说我们说到的内存,两个应用同时访问内存,这个时候每个应用需要知道它访问是哪个,另一个应用访问的是哪个.而在微观上这个时候我需要对它做很好的隔离,我们知道在数据总线上任何一个时刻,只有一个应用去访问存储单元,这就是我们所说的微观上的互斥.

虚拟也就是说我要通过交替运行,使每一个用户感觉到,整个计算机都是,由它一个用户在专门提供服务.如何做到这点实际上就是由操作系统,在每个应用执行的时候这种交替.由于交替的频率非常高,让用户在用的时候感觉不太出来.

异步是指说,由于我们程序是走走停停的,它的行为是不是可预测的.在这里实际上我们需要由操作系统来提供,只要用户的输入是一致的,那么这个时候它的输出结果,就应该是不变的,当然如果说你的那个应用,就是需要知道跟时间相关的,这种走走停停的信息,我们也是可以在操作系统支持之下,能够发现时间上的差异.

对于持久性方面，可以从操作系统中的文件系统支持把数据方便地从磁盘等存储介质上存入和取出来理解。


- 为什么现在的操作系统基本上用C语言来实现？为什么没有人用python，java来实现操作系统？


C语言足够高级，成熟，可以方便编写OS和跨平台；足够底层，能够很好地描述计算机硬件细节；性能有保证,C编译器可以生成高效的机器语言组成的执行代码；C语言产生的一个原因就是为了更好地编写UNIX操作系统。而python, java无法保证性能，不够底层。

---
