---
layout: default
---

**欢迎来到书籍《.NET Core 底层入门》的支持站点！**

**本书主要介绍 .NET Core 公共语言运行时的底层实现，包括异常、多线程、GC 以及 JIT 的实现原理与实现细节。阅读本书可以加深对 .NET 框架的理解，这些知识会在编写框架以及高性能程序时发挥重要的作用，如果您有兴趣，本书中的知识还可以帮助您向 CoreCLR 添加或修改功能并贡献代码，或者实现一个自己的语言框架。**

**本书由中国 NCC 组织 ([.NET Core Community](https://github.com/dotnetcore)) 的两位成员老农(Github: [303248153](https://github.com/303248153)) 与刘浩杨 (Github: [LiuHaoYang](https://github.com/LiuHaoYang)) 编写。老农曾深入阅读过 CoreCLR 的源代码，在博客园上发表过[系列文章](https://www.cnblogs.com/zkweb/category/935426.html)，并编写过 .NET 的 Web 框架 [ZKWeb](https://github.com/zkweb-framework/ZKWeb) 与 C++ 的 Cassandra 驱动 [cpv-cql-driver](https://github.com/cpv-project/cpv-cql-driver)。刘浩杨是 .NET 的 AOP 框架 [AspectCore](https://github.com/dotnetcore/AspectCore-Framework) 的作者，为著名的 APM 框架 [Apache SkyWalking](https://github.com/apache/incubator-skywalking) 提供了 .NET 支持，并在 2018 年获得微软的 MVP 头衔。**

# 章节列表

本书一共 TODO 页，分为 8 章，其中前 4 章是理解 .NET Core 底层实现所需要的基础知识，后 4 章是 .NET Core 底层实现的具体介绍。以下是本书的目录，其中可点击的标题为试读内容，注意试读内容的排版格式与正式书籍会有一些不同。(TODO: 向出版社确认可试读的部分)

## 第一章 - 公共语言运行时概述

- 1.1 - 公共语言运行时概述

## 第二章 - MSIL 入门

- 2.1 - 逆向 .NET 程序到 IL
- 2.2 - 基础语法
- 2.3 - 流程控制
- 2.4 - 类型定义
- 2.5 - 程序集与模块
- 2.6 - 使用 Emit 动态构建代码

## 第三章 - x86 汇编入门

- 3.1 - 汇编与机器码
- 3.2 - 内存
- 3.3 - 寄存器
- 3.4 - 基础指令
- 3.5 - 流程控制
- 3.6 - 函数调用
- 3.7 - 系统调用
- 3.8 - 内存屏障

## 第四章 - 编译与调试 CoreCLR

- 4.1 - 在 Windows 上编译 CoreCLR
- 4.2 - 在 Windows 上调试 CoreCLR
- 4.3 - 在 Linux 上编译 CoreCLR
- 4.4 - 在 Linux 上调试 CoreCLR

## 第五章 - 异常处理实现

- 5.1 - 异常处理简介
- 5.2 - 用户异常的触发
- 5.3 - 硬件异常的触发
- 5.4 - 异常处理实现
- 5.5 - 异常处理对性能的影响

## 第六章 - 多线程实现

- 6.1 - 原生线程
- 6.2 - 托管线程
- 6.3 - 抢占模式与合作模式
- 6.4 - 线程本地储存
- 6.5 - 原子操作
- 6.6 - 自旋锁 (Spinlock)
- 6.7 - 互斥锁 (Mutex)
- 6.8 - 混合锁 (Monitor) 与 lock 语句
- 6.9 - 信号量 (Semaphore)
- 6.10 - 读写锁 (ReaderWriterLock)
- 6.11 - 异步操作
- 6.12 - 执行上下文 (ExecutionContext)
- 6.13 - 同步上下文 (SynchronizationContext)

## 第七章 - GC 垃圾回收实现

- 7.1 - GC 简介
- 7.2 - 对象内存结构
- 7.3 - 托管堆结构
- 7.4 - 分配对象流程
- 7.5 - 垃圾回收流程
- 7.6 - 标记阶段 (Mark)
- 7.7 - 计划阶段 (Plan)
- 7.8 - 重定位阶段 (Relocate)
- 7.9 - 压缩阶段 (Compact)
- 7.10 - 清扫阶段 (Sweep)
- 7.11 - 后台 GC
- 7.12 - 调整 GC 行为
- 7.13 - 获取 GC 信息

## 第八章 - JIT 编译器实现

- 8.1 - JIT 简介
- 8.2 - JIT 编译流程
- 8.3 - IR 结构
- 8.4 - IL 解析 (Importer)
- 8.5 - 函数内联 (Inliner)
- 8.6 - IR 变形 (Morph)
- 8.7 - 流程图分析 (Flowgraph Analysis)
- 8.8 - 本地变量排序 (LclVar Sorting)
- 8.9 - 评价顺序定义 (Tree Ordering)
- 8.10 - 变量版本标记 (SSA & VN)
- 8.11 - 循环优化 (Loop Optimization)
- 8.12 - 赋值传播 (Copy Propagation)
- 8.13 - 公共子表达式消除 (CSE)
- 8.14 - 断言传播 (Assertion Propagation)
- 8.15 - 边界检查消除 (Range Check Elimination)
- 8.16 - 合理化 (Rationalization)
- 8.17 - 低级化 (Lowering)
- 8.18 - 线性扫描寄存器分配 (LSRA)
- 8.19 - 汇编指令生成 (CodeGen)
- 8.20 - 机器代码生成 (Emiiter)
- 8.21 - 函数头信息
- 8.22 - AOT 编译

## 附录

- 1 - 中英文专业名词对照表
- 2 - 常用 IL 指令一览
- 3 - 常用汇编指令一览
- 4 - SOS 扩展命令一览
- 5 - IR 语法树节点类型一览
- 6 - 参考资料一览

# 常见疑问

## 阅读本书需要拥有哪些基础知识？

虽然本书与 .NET Core 源代码的关联比较大，部分章节也会给出相关的源代码链接，但理解本书的内容不需要阅读源代码，本书包含了大量的图表用于解释数据结构与处理流程，如果您是一个拥有一年以上经验的 .NET 开发者，并且对 .NET 运行时底层实现有一定的兴趣，那么应该可以顺利的阅读本书并理解大部分内容。

# 鸣谢列表

本书在编写过程中得到了 .NET 社区中很多网友的支持，包括参与稿件审核、提出建议与提供站点域名等，以下是参与的网友一览，在此对你们表示真心的感谢！

- 刘怡 (Github: [alexinea](https://github.com/alexinea))
- 吴朋飞 (Github: [Skysper](https://github.com/Skysper))
- 吕毅 (Github: [walterlv](https://github.com/walterlv))
- 林德熙 (Github: [lindexi](https://github.com/lindexi))
- 张衡水 (Github: [jonechenug](https://github.com/jonechenug))
- 邹嵩 (Github: [zlzforever](https://github.com/zlzforever))
- 施禹诚 (Github: [linkinshi](https://github.com/linkinshi))
- 杨晓东 (Github: [yang-xiaodong](https://github.com/yang-xiaodong))
- carterHe (TODO)
- SwimmingFish (TODO)
- 全雨秋 (TODO)
- Ivony (TODO)
- hddstiny (TODO)

# 购买方法

本书由北京航空航天大学出版社出版。

购买纸质书籍请访问：[TODO](TODO)<br/>
购买电子书籍请访问：[TODO](TODO)

感谢您的支持！

# 交流讨论

欢迎加入以下 QQ 群组讨论 .NET Core 的底层实现原理、分享高性能程序的开发经验、探讨基础设施的设计方式等。

.NET Core 底层实现交流群：**TODOTODO**

如果您对本书的内容有疑问，也可以到 Github 仓库 [netcoreimpl/questions](https://github.com/netcoreimpl/questions)<br/>
创建 Issue 提问，但回答可能需要几天时间，推荐先在 QQ 群中提问，如果没有解决再创建 Issue。
