```
class X {};
class Y : pubilc virtual X {};
class Z : pubilc virtual X {};
class A : pubilc Y, pubilc Z {};

sizeof(X) = 1
sizeof(Y) = 8
sizeof(Z) = 8
sizeof(A) = 12
```

一个空的类它有一个隐藏的1byte大小，那是被编译前插进去的一个char。这使得这一class的两个对象得以在内存中配置独一无二的地址。

影响类大小的因素：
1. **语言本身造成的额外负担**
2. **编译器对于特殊情况所提供的优化处理**
3. **数据对其的限制**