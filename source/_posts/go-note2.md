---
title: Go笔记(2)
date: 2021-09-29 01:59:25
tags:
    - go
categories:
    - go
---

* [Go变量](#variable)
* [Go工程结构](#struct)
* [Go程序的编译和运行](#compile)
* [IDE工具的使用](#ide)

### <h2 id="variable">Go变量声明和初始化</h2>

1. Go与Java不同，声明变量的类型在变量的名称之后
```
var name type
var i int = 1
```

2. Go的基本类型有

```
bool
string
int、int8、int16、int32、int64
uint、uint8、uint16、uint32、uint64、uintptr
byte // uint8 的别名
rune // int32 的别名 代表一个 Unicode 码
float32、float64
complex64、complex128
```

3. 批量格式

```
var (
	name1 type1
	name2 type2
)
```

4. 简短格式

* 定义变量，同时显式初始化。
* 不能提供数据类型。
* 只能用在函数内部。

```
名字 := 表达式
i, j := 0, 1
x := 100
a, s = 1, ""
```

5. 编译器推导

```
var name
var x = 100
```

