# monkey-go
&lt;&lt;Writing an interpreter>>和&lt;&lt;Writing A Compiler In Go>>两本书的源码

无论是学习go还是深入学习程序执行，编译原理，都强烈推荐这两本书。虽然是英文的，可以在代码程序快速了解编译原理的纵向知识。
当然学习编译原理，还是有很多博大精深的知识点的，这两本书没有一一详解。本书主要从：
1. 如何读取和构造token
2. 在token的基础上如何构造lexer
3. 基于lexer如何做语法解析parser
4. 作为interpreter如何执行解释（eval）parser后的语法树
5. Compiler的作为续集，在前书的基础上使用compiler(vm)执行解析后的代码
6. 其中还可以学到很多go的编程技巧
7. compiler中vm实现程序编译和执行的全过程，对执行块活动记录进行管理
8. vm的执行压栈与出栈和frame结合


## REPL
```shell
go run main.go
```
或者
```shell
go build -o monkey-go && ./monkey-go
```

## 测试
### 编译benchmark
```shell
go build -o fibonacci ./benchmark
```
### 测试对比
```shell
./fibonacci -engine=eval
./fibonacci -engine=vm
```
