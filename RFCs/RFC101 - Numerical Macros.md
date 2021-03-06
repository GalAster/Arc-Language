RFC26 - Numerical Macros



##

浮点数应当被实现为 IEEE 754 64 位双精度值。


0DEAD

- `特殊数值字面量`由0开头表示, 或者用宏标记

非负整数值也可以用十六进制、八进制或二进制来表示.
在这些格式中, （前缀后的）前导零是允许的.

十六进制值大小写不敏感.
下划线仍然可用

数字间的下划线是允许的（但不能存在于前缀和值之间）。

```arc
hex1 = @h`DEADBEEF`  % @h 表示十六进制
hex2 = @h`deadbeef`  % 大小写是无关的
hex3 = @h`dead_beef` % 同样可以使用下划线
oct1 = @o`01234567`  % @o 表示八进制
oct2 = @o`755`       % 对于表示 Unix 文件权限很有用
bin1 = @b`11010110`  % @b 表示二进制
% 带有 `0f` 前缀的浮点数
% 带有 `0i` 前缀的浮点数
```

## 数值字面量

```ts
input: string|number
output: type
```

- 浮点数: `@f8, @f16, @f32, @f64, @f128`

**IEEE 754 所规定的浮点数!**

- 无符号: `@u8, @u16, @u32, @u64, @u128`

- 整数: `@i8, @i16, @i32, @i64, @i128`

- 十六进制: `@h`

- 八进制: `@o`

- 二进制: `@b`

