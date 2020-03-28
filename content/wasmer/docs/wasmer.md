---
date: 2019-09-08T18:00:00+08:00
title: Wasmer Runtime
menu:
  main:
    parent: "wasmer-docs"
weight: 2011
description : "Wasmer Runtime文档"
---

https://docs.wasmer.io/ecosystem/wasmer

Wasmer允许您运行WebAssembly模块，无论是**独立**或**嵌入式**内其他语言，如 C/C++, Rust, Python, Go, PHP, Ruby...

根据设计，WebAssembly模块运行所在的环境与底层主机系统的原生功能完全隔离（或*沙盒化*）。这意味着*默认情况下*，Wasm模块被设计为仅执行纯计算。

因此，通常无法从WASM访问“ 操作系统”级资源，例如文件描述符，网络套接字，系统时钟和随机数。

但是，在许多情况下，Wasm模块需要执行的工作不仅仅是执行纯计算。它们必须与原生“ OS”功能交互。

Wasmer旨在提供三个关键功能：

1. 使程序能够在任何编程语言中运行
2. 使极其便携的二进制文件能够在Wasmer支持的任何“ OS”（例如，Linux，macOS，Windows和FreeBSD）上运行，且无需修改。
3. 充当Wasm模块的安全桥梁， 通过诸如 [`WASI`](https://github.com/webassembly/wasi) 和 [`Emscripten`](https://github.com/emscripten-core/emscripten)（版本1.38.43和更早版本）这样的的应用二进制接口（Application Binary Interfaces/ABI）与原生“ OS”功能交互。

对于第一种情况，我们提供了多种语言集成，允许从任何编程语言中运行相同的Wasm模块。

对于第二种情况，我们提供了独立运行时以在任何平台和芯片组上运行Wasm二进制文件。

重要提示：

> 上面使用的术语“ OS”用引号引起来，表明被调用的原生功能实际上可能不是由主机的操作系统提供的。
>
>实际上，原生函数始终属于运行WebAssembly模块的主机环境，并且可以是主机语言的运行时环境（例如JavaScript，Python或Ruby），也可以是实际的操作系统。 。
>
> 无论哪种方式，从WebAssembly的角度来看，我们都不必太在乎这个细节。我们需要知道的是：
>
> - 主机可以为WebAssembly模块提供“导入”功能
> - 通过Wasmer附带的ABI，WebAssembly模块可以使用不同级别的沙箱访问一组类似于操作系统的功能

