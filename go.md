### 1. new() 和 make() 的区别？

> 首先看看 new() 的函数定义
>
> ```go
> // The new built-in function allocates memory. The first argument is a type,
> // not a value, and the value returned is a pointer to a newly
> // allocated zero value of that type.
> func new(Type) *Type
> ```
>
> 接收一个参数，这个参数是一个类型，分配内存后，返回一个该类型的指针，同时将分配的内存置为 0，
> int 的零值是 0，string 的零值是 ""，引用类型的零值是 nil。
>
> 接下来再看看 make() 的函数定义
>
> ```go
> func make(t Type, size ...IntegerType) Type
> ```
>
> make() 只能用于 `chan` ，map ，slice 的内存创建，返回的是类型本身，因为这三个类型本身就是引用类型。
