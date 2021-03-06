# 第5章 语句

## 5.1 简单语句

#### 空语句

最简单的语句是`空语句（null statement）`，空语句中只含有一个单独的分号：

```cpp
;//空语句
```

#### 复合语句（块）

## 5.2 语句作用域

## 5.3 条件语句

### 5.3.1 if语句

#### 使用 if else 语句

#### 嵌套if语句

#### 注意使用花括号

#### 悬垂else

#### 使用花括号执行路径

### 5.3.2 switch语句

## 5.4 迭代语句

### 5.4.1 while语句

#### 使用while循环

### 5.4.2 传统的for语句

### 5.4.3 范围for语句

### 5.4.4 do while 语句

## 5.5 跳转语句

### 5.5.1 break语句

### 5.5.2 continue语句

### 5.5.3 goto 语句

**goto语句（goto statement）**的作用是从goto语句无条件跳转到同一函数内的另一条语句。

goto语句的语法形式是：

```text
goto label:
```

其中，`label`是用于标识一条语句的标示符，\*\*带标签的语句（labeled statement）是一种特殊的语句，在它之前有一个标示符以及一个冒号：

```text
end: return;
```

和`switch`语句类似，`goto`语句也不能将程序的控制权从变量的作用域之外转移到作用域之内：

```cpp
goto end;
int ix = 10; //错误：goto语句绕过了一个带初始化的变量定义
end: ix = 42; //错误：此处的代码需要使用ix，但是goto语句绕过了它的声明。
```

## 5.6 try语句块和异常处理

异常处理机制为程序中异常检测和异常处理这两部分的协作提供支持。在`C++`语言中，异常处理包括：

* throw表达式，异常检测部分使用throw表达式来表示它遇到了无法处理的问题。我们说throw引发了异常。
* try语句块，异常处理部分使用try语句块处理异常。try语句块以关键字try开始，并以一个或多个catch子句结束。try语句块中代码抛出的异常通常会被某个catch子句结束。try语句块中代码抛出的异常通常会被某个catch子句处理。因为catch子句处理异常，所以它们也被称作异常处理代码。
* 一套异常类，用于在throw表达式和相关的catch子句之间传递异常的具体信息。

### 5.6.1 throw表达式

### 5.6.2 try语句块

#### 编写处理代码

#### 函数在寻找处理代码的过程中退出

### 5.6.3 标准异常

