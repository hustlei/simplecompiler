## 简介
实现一个最简单的编译器。

为了简洁易懂，编译器仅支持以下简单功能：

+ 数据类型只支持整形
+ 变量名只能为一到多个英文字母组成
+ 支持`加(+)`，`加(-)`以及`赋值(=)`运算
+ 每个赋值语句或者运算语句以换行表示结束

> 为方便检查结果，默认打印最后一个表达式计算值

## 源文件说明

+ lexer.l: Flex源文件，用于词法分析，识别源代码输出token。
+ parer.y: Bison源文件，用于语法分析，根据token输出抽象语法树。
+ ast.h：抽象语法树(Abstract Syntax Tree)定义代码。
+ genIR.cpp：调用llvm把抽象语法树转换为ir。
+ compiler.cpp：编译器主程序。
+ sample：文件夹内包含示例

## 示例