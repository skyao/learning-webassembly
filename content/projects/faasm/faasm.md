---
date: 2020-03-21T09:00:00+08:00
title: Faasm概述
weight: 1
description : "Faasm概述"
---

### Faasm介绍

https://github.com/lsds/Faasm

> High-performance stateful serverless runtime based on WebAssembly
>
> 基于 WebAssembly 的高性能有状态serverless运行时

Faasm是一种高性能的有状态serverless运行时。

Faasm提供多租户隔离，但也允许函数共享内存区域。这些共享内存区域提供了低延迟并发访问数据的功能，并且在全局范围内同步以支持大规模并行。

Faasm将WebAssembly的软件故障隔离与标准Linux工具结合在一起，以低成本提供安全性和资源隔离。 Faasm并排运行函数，并作为单个运行时进程的线程，具有较低的开销和快速的启动时间。底层的WebAssembly执行和代码生成由WAVM处理。

Faasm定义了一个自定义的主机接口，该接口使函数可以执行无服务器特定的任务（例如调用其他函数和管理状态）以及与底层主机进行交互（例如使用文件系统和网络）。 Faasm主机接口实现了与WASI相同的目标，但是在无服务器特定的上下文中。