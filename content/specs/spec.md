---
date: 2020-05-13T18:00:00+08:00
title: 规范概述
weight: 201
description : "Wasm规范概述"
---

Wasm规范内容：

- https://webassembly.github.io/spec/
- https://github.com/WebAssembly/spec

为了支持将WebAssembly嵌入到不同的环境中，它的规范被分割成不同的层，并在不同的文档中指定。

### 核心规范

定义了独立于具体嵌入的WebAssembly模块的语义。WebAssembly核心在一个单独文档中指定了WebAssembly Core。

* WebAssembly：定义了WebAssembly模块的结构、指令集、二进制和文本格式的表示方式以及验证、实例化和执行的语义。

	- https://webassembly.github.io/spec/core/bikeshed/

### 嵌入器规格

定义应用程序编程接口（API），使WebAssembly模块能够在具体的嵌入环境中使用。目前，制订了两个API：

1. JavaScript Embedding：定义了从JavaScript中访问WebAssembly的JavaScript类和对象，包括用于验证、编译、实例化的方法，以及作为JavaScript对象表示和操作导入和导出的类。

	https://webassembly.github.io/spec/js-api/index.html

2. Web Embedding：定义了专门在Web浏览器中提供的JavaScript API的扩展，特别是一个用于流式编译和从源绑定的Response类型实例化的接口。

	https://webassembly.github.io/spec/web-api/index.html








