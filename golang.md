## 2.2声明

var、const、type和func，分别对应变量、常量、类型和函数实体对象 

## 2.3变量

如果初始化表达式被省略，那么将用零值初始化该变 量。 

**数值类型**变量对应的零值是0，**布尔类型变量**对应的零值是false，**字符串类型**对应的零值是空字符串，**接口或引用**类型(包括slice、map、chan和函数)变量对应的零值是nil。**数组或结构体等**聚合类型对应的零值是每个元素或字段都是对应该类型的零值 。

go语言中不存在未初始化的变量。

### 2.3.1 简短变量声明 

可用于声明和初始化局部变量 .

```
freq := rand.Float64() * 3.0
```

### 2.3.2 指针

如果用“var x int”声明语句声明一个x变量，那么&x表达式(取x变量的内存地址)将产生一个 指向该整数变量的指针，指针对应的数据类型是 *int ，指针被称之为“指向int类型的指针”。 一般 *p 表达式读取指针指向的变量的值 

在Go语言中，返回函数中局部变量的地址也是安全的。例如下面的代码，调用f函数时创建局 部变量v，在局部变量地址被返回之后依然有效，因为指针p依然引用这个变量。 

```
var p = f() 
func f() *int {
    v := 1
    return &v } 
```

每次调用f函数都将返回不同的结果: 

```
fmt.Println(f() == f()) // "false"
```

### 2.3.3 new函数

另一个创建变量的方法是调用用内建的new函数。表达式new(T)将创建一个T类型的匿名变 

量，初始化为T类型的零值，然后返回变量地址，返回的指针类型为 *T 。 

### 2.3.4. 变量的生命周期 