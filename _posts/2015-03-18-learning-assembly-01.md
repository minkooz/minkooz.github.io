---
title: "汇编语言笔记 (1)"
---

# 基本概念

MASM 可以建立一下种类的程序


* 32bit 保护模式 *运行于 32-bit Windows 系统*
* 64bit 模式 *运行于 64-bit Windows 系统*
* 16bit 实地址模式 *运行于 32-bit Windows 系统* 和 *嵌入系统*，不被 64-bit 系统支持。

> 疑问：64bit 系统运行32bit 保护模式？


 汇编语言指令和机器语言是一对一的。
 CPU 指令的两个操作数必须大小相同。`note: 相对于高级语言的限制更少，但仍有限制）`

练习：

C语言


    int Y;
	int X = ( Y + 4) * 3;

汇编语言

	mov  eax, Y
	add  eax, 4
	mov  ebx, 3
	imul ebx
	mov  X, eax

> 疑问：为什么不是
> 
> 	mov  eax, Y
> 	add  eax, 4
> 	imul eax, 3
> 	mov  X, eax





## 