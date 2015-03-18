---
title: "汇编语言笔记 (1)"
---

从本篇开始，记录汇编语言的学习过程。教材使用 [Assembly Language for x86 Processors (7th Edition)](http://www.asmirvine.com/) 

## 综述

MASM 可以建立以下种类的程序：


* 32bit 保护模式 *运行于 32-bit Windows 系统*
* 64bit 模式 *运行于 64-bit Windows 系统*
* 16bit 实地址模式 *运行于 32-bit Windows 系统* 和 *嵌入系统*，不被 64-bit 系统支持。

> 疑问：64bit 系统运行32bit 保护模式？


 汇编语言指令和机器语言是一对一的。高级语言与汇编语言的指令是一对多的。
 
> 汇编语言相对于高级语言的限制更少，但仍受限于处理器和其对应的机器语言，例如，CPU 要求指令的两个操作数必须大小相同。

【例子】

C语言：


    int Y;
	int X = ( Y + 4) * 3;

汇编语言：

	mov  eax, Y
	add  eax, 4
	mov  ebx, 3
	imul ebx
	mov  X, eax

> 疑问：为什么不可以这样写：
> 
> 	mov  eax, Y
> 	add  eax, 4
> 	imul eax, 3
> 	mov  X, eax


## 虚拟机的层次

> 深入阅读：Andrew Tanenbaum's *Structured Computer Organization*

* Level 1 数字逻辑 
* Level 2 指令集架构（ISA）*程序使用机器语言*
* Level 3 汇编语言 *可轻易转译 ISA*
* Level 4 高级语言

## 进制

使用二进制，十六进制，并熟悉与十进制之间的互相换算方法。