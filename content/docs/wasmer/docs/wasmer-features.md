---
date: 2019-09-08T18:00:00+08:00
title: Wasmer Feature
weight: 2012
description : "Wasmer Feature文档"
---

https://docs.wasmer.io/ecosystem/wasmer/wasmer-features

Wasmer WebAssembly运行时为用户和开发人员提供了各种功能：

- **后端：** Wasmer支持多个编译器后端：*Singlepass*，*Cranelift*和*LLVM*。这些中的每一个在编译速度与运行速度之间都有不同的权衡。
- **缓存**：可以重复使用已编译的WebAssembly模块，因此后续运行Wasm文件的启动时间很短
- **计量**：可以监视计算时间和其他资源，并可以设置限制来控制Wasm代码的运行方式。这也称为“gas metering/气体计量”
- *WebAssembly功能*：
	- **多值返回**：从函数返回多个值，使host和guest之间的数据传输更加简单
	- **SIMD**：单指令，多数据：更快地执行重数运算和/或以更低的功耗使用
- ABI：它允许使用ABI运行编译到WebAssembly的不同类型的程序，例如：
	- **Emscripten**
	- **WASI**

详细支持情况看原文。

备注：Rust 的支持还是挺好的。