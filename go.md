### 1. new 和 make 的区别？

> 首先看看 new 和 make 的函数定义
>
> ```go
> // The new built-in function allocates memory. The first argument is a type,
> // not a value, and the value returned is a pointer to a newly
> // allocated zero value of that type.
> func new(Type) *Type
> ```
