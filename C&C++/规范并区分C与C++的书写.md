# 规范并区分C与C++的书写
C++向下兼容C，大量的具体语法与C相同或类同，基本可以使用C的代码。但是，C++与C是存在很大不同的。编程思维和许多细节上的理念是有大不同的；同样的功能C++有新定义的语法，甚至是新的实现方式；C与C++语法的自由性可能性不同，导致了程序的安全性多元性不同。同时C++相对于C拓充了许多新功能，以及对某些代码的功能进行了放缩调整。混用C与C++语法可能造成编写代码或后期阅读时的混乱。因此明确的区分当前是在使用C还是C++来编写代码是必要的。
# 相同功能但格式不同
## 显式的类型转换
C的格式：
```c
(int)value;
//(typeName)value
```
C++的格式：
```c++
int(value);
static_cast<int>(value);
//typeName(value)
//static_cast<typeName>(value)
//static_cast<>为4个强制类型转换符之一，它们的使用要求比较严格，从而规避C语言式的强制类型转换因过多可能性而带来的危险
```
# C++新增特性
## 数据类型
`long long` `unsigned long long`字面上更加强调是`int`的宽度拓展。  
`wchar_t`它的宽度取决于实现。可以存储系统的扩展字符集的任意成员。  
`char16_t` `char32_t`它们的宽度分别可以存储16位(2字节)和32位(4字节)的字符编码。确保字符型足够大，能够存储系统的基本字符集中的任何成员。
