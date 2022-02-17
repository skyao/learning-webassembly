---
date: 2022-02-17T18:00:00+08:00
title: wapm安装
weight: 100
description : "wapm安装"
---

## 安装

参考 https://docs.wasmer.io/ecosystem/wasmer/getting-started ：

```bash
$ curl https://get.wasmer.io -sSfL | sh

Welcome to the Wasmer bash installer!

               ww
               wwwww
        ww     wwwwww  w
        wwwww      wwwwwwwww
ww      wwwwww  w     wwwwwww
wwwww      wwwwwwwwww   wwwww
wwwwww  w      wwwwwww  wwwww
wwwwwwwwwwwwww   wwwww  wwwww
wwwwwwwwwwwwwww  wwwww  wwwww
wwwwwwwwwwwwwww  wwwww  wwwww
wwwwwwwwwwwwwww  wwwww  wwwww
wwwwwwwwwwwwwww  wwwww   wwww
wwwwwwwwwwwwwww  wwwww
   wwwwwwwwwwww   wwww
       wwwwwwww
           wwww

downloading: wasmer-linux-amd64
Latest release: 2.2.0-rc2
Downloading archive from https://github.com/wasmerio/wasmer/releases/download/2.2.0-rc2/wasmer-linux-amd64.tar.gz
######################################################################## 100.0%######################################################################### 100.0%
installing: /home/sky/.wasmer
Updating bash profile /home/sky/.zshrc
we've added the following to your /home/sky/.zshrc
If you have a different profile please add the following:

# Wasmer
export WASMER_DIR="/home/sky/.wasmer"
[ -s "$WASMER_DIR/wasmer.sh" ] && source "$WASMER_DIR/wasmer.sh"
check: wasmer 2.2.0-rc2 installed successfully ✓
wasmer & wapm will be available the next time you open the terminal.
If you want to have the commands available now please execute:

source /home/sky/.wasmer/wasmer.sh

```

验证安装：

```bash
$ source /home/sky/.wasmer/wasmer.sh
$ wapm --version                                                        
wapm-cli 0.5.1

$ which wapm    
/home/sky/.wasmer/bin/wapm
```

## 示例

