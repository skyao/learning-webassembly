---
date: 2012-02-17T18:00:00+08:00
title: Binaryen概述
weight: 1
description : "Binaryen概述"
---

## 介绍

http://webassembly.github.io/binaryen/

> Compiler infrastructure and toolchain library for WebAssembly
>
> 用于WebAssembly的编译器基础设施和工具链库

Binaryen是一个用C++编写的WebAssembly的编译器和工具链基础库。它的目的是使编译到WebAssembly变得简单、快速和有效。

- **简单**：Binaryen有一个简单的C语言API，有一个头文件，也可以从JavaScript使用。它接受类似WebAssembly形式的输入，但也接受一般控制流图，供喜欢的编译器使用。

- **快速**。Binaryen的内部IR使用紧凑的数据结构，并被设计为完全并行的代码生成和优化，使用所有可用的CPU核心。Binaryen的IR还可以非常容易和快速地编译成WebAssembly，因为它基本上是WebAssembly的一个子集。

- **有效**。Binaryen的优化器有许多环节可以非常显著地改善代码（例如，局部着色以凝聚局部变量；消除死代码；在编译时尽可能地预计算表达式；等等）。这些优化的目的是使Binaryen强大到可以单独作为一个编译器后端使用。一个特定的重点领域是针对WebAssembly的优化（通用编译器可能做不到），你可以把它看作是wasm minification，类似于JavaScript、CSS等的minification，所有这些都是特定的语言（这种优化的一个例子是SimplifyLocals的块返回值生成）。

使用Binaryen构建的编译器包括：

- asm2wasm，将asm.js编译为WebAssembly。
- AssemblyScript，它将TypeScript编译成Binaryen IR
- wasm2js，将WebAssembly编译为JS。
- Asterius，将Haskell编译为WebAssembly。

Binaryen还提供了一套工具链实用程序，可以:

- 解析和发射WebAssembly。特别是，这可以让你加载WebAssembly，用Binaryen优化它，然后重新释放它，从而在一个命令中实现wasm到wasm的优化器。
- 解释WebAssembly以及运行WebAssembly规范测试。
- 与Emscripten集成，以便提供一个完整的编译器工具链，从C和C++到WebAssembly。
- 如果浏览器还没有本地支持，可以通过在编译成JavaScript的解释器中运行WebAssembly来实现Polyfill（对测试有用）。




## 信息

### 网站

- [github](https://github.com/WebAssembly/binaryen)

### 介绍内容

- [COMPILING TO WEBASSEMBLY WITH BINARYEN](https://kripken.github.io/talks/binaryen.html#/): 2016年