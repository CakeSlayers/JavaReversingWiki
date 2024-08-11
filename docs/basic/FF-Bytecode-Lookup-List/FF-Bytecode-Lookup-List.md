# 前言

这里是被Java字节码库 *([ASM](https://asm.ow2.io/))* 简化过的Java字节指令码列表 .
这里的简明Java字节指令码是Recaf及其他字节码编辑/查看器采用的字节指令码标准[（官方字节指令码表）](https://docs.oracle.com/javase/specs/jvms/se12/html/jvms-6.html)

# 目录

[TOC]

# 指令

| 操作码         | 操作栈（按从栈底到栈顶的顺序排列）: [之前]→[之后]             | 描述                                                                                                                                                                         |
|----------------|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `aconst_null`  | → `null`                                                    | `null` 值入栈                                                                                                                                                                |
| `dconst_0`     | → `0.0`                                                     | 常量 `0.0` (double)值入栈                                                                                                                                                    |
| `dconst_1`     | → `1.0`                                                     | 常量 `1.0` (double)值入栈                                                                                                                                                    |
| `fconst_0`     | → `0.0f`                                                    | `0.0f` (float) 值入栈                                                                                                                                                        |
| `fconst_1`     | → `1.0f`                                                    | `1.0f` (float)值入栈                                                                                                                                                         |
| `fconst_2`     | → `2.0f`                                                    | `2.0f` (float)值入栈                                                                                                                                                         |
| `iconst_m1`    | → `-1`                                                      | -1(int)值入栈                                                                                                                                                                |
| `iconst_0`     | → `0`                                                       | 0(int)值入栈                                                                                                                                                                 |
| `iconst_1`     | → `1`                                                       | 1(int)值入栈                                                                                                                                                                 |
| `iconst_2`     | → `2`                                                       | 2(int)值入栈                                                                                                                                                                 |
| `iconst_3`     | → `3`                                                       | 3(int)值入栈                                                                                                                                                                 |
| `iconst_4`     | → `4`                                                       | 4(int)值入栈                                                                                                                                                                 |
| `iconst_5`     | → `5`                                                       | 5(int)值入栈                                                                                                                                                                 |
| `lconst_0`     | → `0L`                                                      | 0L(long)值入栈                                                                                                                                                               |
| `lconst_1`     | → `1L`                                                      | 1L(long)值入栈                                                                                                                                                               |
| `arraylength`  | <数组引用>→ <数组长度>                                      | 获取数组长度                                                                                                                                                                 |
| `aaload`       | <数组引用>, <索引> → 值                                     | 从引用类型数组中入栈指定项的值                                                                                                                                               |
| `aastore`      | <数组引用>, <索引>, 值 →                                    | 将栈顶引用类型值储存到指定引用类型数组的指定项                                                                                                                               |
| `baload`       | <数组引用>, <索引> → 值                                     | 从 `boolean` 类型数组或 `byte` 类型数组中入栈指定项的值                                                                                                                      |
| `bastore`      | <数组引用>, <索引>, 值 →                                    | 将栈顶 `boolean` 类型值或 `byte` 类型值储存到指定 `boolean` 类型数组或 `byte` 类型数组的指定项                                                                               |
| `caload`       | <数组引用>, <索引> → 值                                     | 将 `char` 型数组指定索引的值入栈                                                                                                                                             |
| `castore`      | <数组引用>, <索引>, 值 →                                    | 将栈顶 `char` 类型值储存到对应类型数组的指定项                                                                                                                               |
| `daload`       | <数组引用>, <索引> → 值                                     | 将 `double` 型数组指定索引的值推送至栈顶                                                                                                                                     |
| `dastore`      | <数组引用>, <索引>, 值 →                                    | 将栈顶 `double` 类型值储存到对应类型数组的指定项                                                                                                                             |
| `faload`       | <数组引用>, <索引> → 值                                     | 将 `float` 型数组指定索引的值推送至栈顶                                                                                                                                      |
| `fastore`      | <数组引用>, <索引>, 值 →                                    | 将栈顶 `float` 类型值储存到对应类型数组的指定项                                                                                                                              |
| `iaload`       | <数组引用>, <索引> → 值                                     | 将 `int` 型数组指定索引的值推送至栈顶                                                                                                                                        |
| `iastore`      | <数组引用>, <索引>, 值 →                                    | 将栈顶 `int` 类型值储存到对应类型数组的指定项                                                                                                                                |
| `laload`       | <数组引用>, <索引> → 值                                     | 将 `long` 型数组指定索引的值推送至栈顶                                                                                                                                       |
| `lastore`      | <数组引用>, <索引>, 值 →                                    | 将栈顶 `long` 类型值储存到对应类型数组的指定项                                                                                                                               |
| `saload`       | <数组引用>, <索引> → 值                                     | 将 `short` 型数组指定索引的值推送至栈顶                                                                                                                                      |
| `sastore`      | <数组引用>, <索引>, 值 →                                    | 将栈顶 `short` 类型值储存到对应类型数组的指定项                                                                                                                              |
| `d2f`          | 值 → <结果>                                                 | 类型转换: `double` 到 `float`                                                                                                                                                |
| `d2i`          | 值 → <结果>                                                 | 类型转换: `double` 到 `int`                                                                                                                                                  |
| `d2l`          | 值 → <结果>                                                 | 类型转换: `double` 到 `long`                                                                                                                                                 |
| `f2d`          | 值 → <结果>                                                 | 类型转换: `float` 到 `double`                                                                                                                                                |
| `f2i`          | 值 → <结果>                                                 | 类型转换: `float` 到 `int`                                                                                                                                                   |
| `f2l`          | 值 → <结果>                                                 | 类型转换: `float` 到 `long`                                                                                                                                                  |
| `i2b`          | 值 → <结果>                                                 | 类型转换: `int` 到 `byte`                                                                                                                                                    |
| `i2c`          | 值 → <结果>                                                 | 类型转换: `int` 到 `char`                                                                                                                                                    |
| `i2d`          | 值 → <结果>                                                 | 类型转换: `int` 到 `double`                                                                                                                                                  |
| `i2f`          | 值 → <结果>                                                 | 类型转换: `int` 到 `float`                                                                                                                                                   |
| `i2l`          | 值 → <结果>                                                 | 类型转换: `int` 到 `long`                                                                                                                                                    |
| `i2s`          | 值 → <结果>                                                 | 类型转换: `int` 到 `short`                                                                                                                                                   |
| `l2d`          | 值 → <结果>                                                 | 类型转换: `long` 到 `double`                                                                                                                                                 |
| `l2f`          | 值 → <结果>                                                 | 类型转换: `long` 到 `float`                                                                                                                                                  |
| `l2i`          | 值 → <结果>                                                 | 类型转换: `long` 到 `int`                                                                                                                                                    |
| `areturn`      | 引用 → [堆栈销毁]                                           | 返回一个引用                                                                                                                                                                 |
| `dreturn`      | 值 → [堆栈销毁]                                             | 返回一个 `double`                                                                                                                                                            |
| `freturn`      | 值 → [堆栈销毁]                                             | 返回一个 `float`                                                                                                                                                             |
| `ireturn`      | 值 → [堆栈销毁]                                             | 返回一个 `int`                                                                                                                                                               |
| `lreturn`      | 值 → [堆栈销毁]                                             | 返回一个 `long`                                                                                                                                                              |
| `return`       | → [堆栈销毁]                                                | 直接返回 ( `void` )                                                                                                                                                          |
| `dadd`         | 值1, 值2 → <结果>                                           | 将两个 `double` 值相加并入栈                                                                                                                                                 |
| `ddiv`         | 值1, 值2 → <结果>                                           | 将两个 `double` 值相除并入栈                                                                                                                                                 |
| `dmul`         | 值1, 值2 → <结果>                                           | 将两个 `double` 值相乘并入栈                                                                                                                                                 |
| `drem`         | 值1, 值2 → <结果>                                           | 将两个 `double` 值取模并入栈, 计算规则: `(值2 - ((值1 / 值2) * 值2))`                                                                                                        |
| `dsub`         | 值1, 值2 → <结果>                                           | 将两个 `double` 值相减并入栈                                                                                                                                                 |
| `fadd`         | 值1, 值2 → <结果>                                           | 将两个 `float` 值相加并入栈                                                                                                                                                  |
| `fdiv`         | 值1, 值2 → <结果>                                           | 将两个 `float` 值相除并入栈                                                                                                                                                  |
| `fmul`         | 值1, 值2 → <结果>                                           | 将两个 `float` 值相乘并入栈                                                                                                                                                  |
| `frem`         | 值1, 值2 → <结果>                                           | 将两个 `float` 值取模并入栈, 计算规则:  `(值2 - ((值1 / 值2) * 值2))`                                                                                                        |
| `fsub`         | 值1, 值2 → <结果>                                           | 将两个 `float` 值相减并入栈                                                                                                                                                  |
| `iadd`         | 值1, 值2 → <结果>                                           | 将两个 `int` 值相加并入栈                                                                                                                                                    |
| `idiv`         | 值1, 值2 → <结果>                                           | 将两个 `int` 值相除并入栈                                                                                                                                                    |
| `imul`         | 值1, 值2 → <结果>                                           | 将两个 `int` 值相乘并入栈                                                                                                                                                    |
| `irem`         | 值1, 值2 → <结果>                                           | 将两个 `int` 值取模并入栈, 计算规则:  `(值2 - ((值1 / 值2) * 值2))`                                                                                                          |
| `isub`         | 值1, 值2 → <结果>                                           | 将两个 `int` 值相减并入栈                                                                                                                                                    |
| `iand`         | 值1, 值2 → <结果>                                           | 执行位运算 `值1 & 值2` 并将结果入栈                                                                                                                                          |
| `ior`          | 值1, 值2 → <结果>                                           | 执行位运算 `值1 \| 值2` 并将结果入栈                                                                                                                                         |
| `ixor`         | 值1, 值2 → <结果>                                           | 执行位运算 `值1 \^ 值2` 并将结果入栈                                                                                                                                         |
| `ishl`         | 值1, 值2 → <结果>                                           | 执行位运算 `值1 << 值2的低五位` 并将结果入栈                                                                                                                                 |
| `ishr`         | 值1, 值2 → <结果>                                           | 执行位运算 `值1 >> 值2的低五位` 并将结果入栈                                                                                                                                 |
| `iushr`        | 值1, 值2 → <结果>                                           | 执行位运算 `值1 >>> 值2的低五位` 并将结果入栈                                                                                                                                |
| `ladd`         | 值1, 值2 → <结果>                                           | 将两个 `long` 值相加并入栈                                                                                                                                                   |
| `ldiv`         | 值1, 值2 → <结果>                                           | 将两个 `long` 值相除并入栈                                                                                                                                                   |
| `lmul`         | 值1, 值2 → <结果>                                           | 将两个 `long` 值相乘并入栈                                                                                                                                                   |
| `lrem`         | 值1, 值2 → <结果>                                           | 将两个 `long` 值取模并入栈, 计算规则:  `(值2 - ((值1 / 值2) * 值2))`                                                                                                         |
| `lsub`         | 值1, 值2 → <结果>                                           | 将两个 `long` 值相减并入栈                                                                                                                                                   |
| `lshl`         | 值1, 值2 → <结果>                                           | 执行位运算 `值1 << 值2的低五位` 并将结果入栈                                                                                                                                 |
| `lshr`         | 值1, 值2 → <结果>                                           | 执行位运算 `值1 >> 值2的低五位` 并将结果入栈                                                                                                                                 |
| `lushr`        | 值1, 值2 → <结果>                                           | 执行位运算 `值1 >>> 值2的低五位` 并将结果入栈                                                                                                                                |
| `land`         | 值1, 值2 → <结果>                                           | 执行位运算 `值1 & 值2` 并将结果入栈                                                                                                                                          |
| `lor`          | 值1, 值2 → <结果>                                           | 执行位运算 `值1 \| 值2` 并将结果入栈                                                                                                                                         |
| `lxor`         | 值1, 值2 → <结果>                                           | 执行位运算 `值1 \^ 值2` 并将结果入栈                                                                                                                                         |
| `dneg`         | 值 → <结果>                                                 | 取反 `double`  `-值`                                                                                                                                                         |
| `fneg`         | 值 → <结果>                                                 | 取反 `float`  `-值`                                                                                                                                                          |
| `ineg`         | 值 → <结果>                                                 | 取反 `int`  `-值`                                                                                                                                                            |
| `lneg`         | 值 → <结果>                                                 | 取反 `long`  `-值`                                                                                                                                                           |
| `dcmpg`        | 值1, 值2 → <`int` 结果>                                     | 比较两个 `double`。如果值1>值2，1入栈;如果值1==值2，0入栈；如果值1<值2，-1入栈；如果两者有其一为Nan则1入栈                                                                         |
| `dcmpl`        | 值1, 值2 → <`int` 结果>                                     | 比较两个 `double`。如果值1>值2，-1入栈;如果值1==值2，0入栈；如果值1<值2，1入栈；如果两者有其一为Nan则-1入栈                                                                        |
| `fcmpg`        | 值1, 值2 → <`int` 结果>                                     | 比较两个 `float`。如果值1>值2，1入栈;如果值1==值2，0入栈；如果值1<值2，-1入栈；如果两者有其一为Nan则1入栈                                                                          |
| `fcmpl`        | 值1, 值2 → <`int` 结果>                                     | 比较两个 `float`。如果值1>值2，-1入栈;如果值1==值2，0入栈；如果值1<值2，1入栈；如果两者有其一为Nan则-1入栈                                                                         |
| `lcmp`         | 值1, 值2 → <`int` 结果>                                     | 比较两个 `long`。 如果值1>值2，1入栈;如果值1==值2，0入栈；如果值1<值2，-1入栈；如果两者有其一为Nan则1入栈                                                                          |
| `athrow`       | objectref → [empty], objectref                              | 抛出异常，栈被清空后将objectref推入栈顶并跳转到对应的handler )*                                                                                                               |
| `dup`          | 值 → 值, 值                                                 | 复制栈顶的值，并将其推入栈顶                                                                                                                                                  |
| `dup_x1`       | 值2, 值1 → 值1, 值2, 值1                                    | 将栈顶元素复制并插入到栈的第三个位置。 `值1` 和 `值2` 的类型必须不能为 `double` 或者 `long` .                                                                                 |
| `dup_x2`       | 值3, 值2, 值1 → 值1, 值3, 值2, 值1                          | 将栈顶元素复制并插入到栈的第三 *(如果 `值2` 为 `double` 或者 `long`，他将占用 `值3` 的位置)* 或者第四 (`值2` 不是 `double` 或者 `long` ) 个值处。`值3`不能为`double`或者`long` |
| `dup2`         | {值2, 值1} → {值2, 值1}, {值2, 值1}                         | 复制栈顶的两个值 *(两个值, 如果 `值1` 是 `double` 或者 `long`; 或者一个值, 如果 `值1` 不是 `double` 或者 `long` )* 。 `值2`不能为`double`或者`long`                           |
| `dup2_x1`      | 值3, {值2, 值1} → {值2, 值1}, 值3, {值2, 值1}               | 复制栈顶的两个值并且插入到第三个值下面 *(见上面的解释)*                                                                                                                      |
| `dup2_x2`      | {值4, 值3}, {值2, 值1} → {值2, 值1}, {值4, 值3}, {值2, 值1} | 复制栈顶的两个值并且插入到第四个值下面                                                                                                                                       |
| `pop`          | 值 →                                                        | 从栈顶丢弃一个值                                                                                                                                                             |
| `pop2`         | {值2, 值1} →                                                | 从栈顶丢弃两个值 *(或者一个值，如果栈顶元素为 `double` or `long`)*                                                                                                            |
| `swap`         | 值2, 值1 → 值1, 值2                                         | 交换栈顶的两个值 *( `值1` 和 `值2` 不能是 `double` or `long`)*                                                                                                               |
| `monitorenter` | 引用 →                                                      | 进入同步块，获取对象的锁                                                                                                                                                      |
| `monitorexit`  | 引用 →                                                      | 退出同步块，释放对象的锁                                                                                                                                                      |
| `nop`          | [无变化]                                                    | 无操作                                                                                                                                                                       |

# Integer

| Opcode                | Stack: [before]→[after] | Description                              |
|-----------------------|-------------------------|------------------------------------------|
| `bipush` 值           | → 值                    | 将一个 `byte` 值以 `int` 推入栈顶        |
| `sipush` 值           | → 值                    | 将一个 `short` 值以 `int` 推入栈顶       |
| `newarray` descriptor | count → <数组引用>      | 创建长度为`count`的数组 （类型描述符如下） |

|  类型   | 描述符缩写 |
|:-------:|:----------:|
| boolean |     Z      |
|  char   |     C      |
|  float  |     F      |
| double  |     D      |
|  byte   |     B      |
|  short  |     S      |
|   int   |     I      |
|  long   |     J      |
|  void   |     v      |

# Variable

| Opcode         | Stack: [before]→[after] | Description                             |
|----------------|-------------------------|-----------------------------------------|
| `iload` index  | → 值                    | 从局部变量<index>处加载一个  `int` 值   |
| `lload` index  | → 值                    | 从局部变量<index>处加载一个 `long` 值   |
| `fload` index  | → 值                    | 从局部变量<index>处加载一个 `float` 值  |
| `dload` index  | → 值                    | 从局部变量<index>处加载一个 `double` 值 |
| `aload` index  | → objectref             | 从局部变量<index>处加载一个引用类型的值 |
| `istore` index | 值 →                    | 往局部变量<index>处储存一个  `int` 值   |
| `lstore` index | 值 →                    | 往局部变量<index>处储存一个 `long` 值   |
| `fstore` index | 值 →                    | 往局部变量<index>处储存一个 `float` 值  |
| `dstore` index | 值 →                    | 往局部变量<index>处储存一个 `double` 值 |
| `astore` index | objectref →             | 往局部变量<index>处储存一个引用类型的值 |

# Type

| Opcode            | Stack: [before]→[after] | Description                                                       |
|-------------------|-------------------------|-------------------------------------------------------------------|
| `new` type        | → objectref             | 创建类型为`type`的对象并入栈                                      |
| `anewarray` type  | count → <数组引用>      | 创建一个长度为 `count` ，成员类型为`type`的数组                    |
| `checkcast` type  | objectref → objectref   | 将栈顶成员强转为`type`类型，如果转换失败则抛出`ClassCastException` |
| `instanceof` type | objectref → <结果>      | 检测 `objectref` 是否为 `type`                                    |

# Field

| Opcode                      | Stack: [before]→[after] | Description                                                        |
|-----------------------------|-------------------------|--------------------------------------------------------------------|
| `getfield` owner name desc  | objectref → 值          | 从 `owner` 的实例获取一个名称为 `name` ，描述符为 `desc` 的字段     |
| `getstatic` owner name desc | → 值                    | 从 `owner` 获取一个名称为 `name` ，描述符为 `desc` 的静态字段       |
| `putfield` owner name desc  | objectref, 值 →         | 将`值`存储到 `owner` 的实例中名称为 `name` ，描述符为 `desc` 的字段 |
| `putstatic` owner name desc | 值 →                    | 将`值`存储到 `owner` 中名称为 `name` ，描述符为 `desc` 的静态字段   |

# Method

| Opcode                            | Stack: [before]→[after]               | Description                                                                                                                 |
|-----------------------------------|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| `invokeinterface` owner name desc | objectref, [arg1, arg2, ...] → <结果> | 调用接口 `owner` 中名称为 `name` ，描述符为 `desc` 的方法，接口的实现为 `objectref` 对象，如果返回值类型不为`void`则返回值入栈 |
| `invokespecial` owner name desc   | objectref, [arg1, arg2, ...] → <结果> | 调用类 `owner` 中名称为 `name` ，描述符为 `desc` 的非虚方法， `objectref` 为类的实例，如果返回值类型不为`void`则返回值入栈     |
| `invokestatic` owner name desc    | [arg1, arg2, ...] → <结果>            | 调用类 `owner` 中名称为 `name` ，描述符为 `desc` 的静态方法，如果返回值类型不为`void`则返回值入栈                             |
| `invokevirtual` owner name desc   | objectref, [arg1, arg2, ...] → <结果> | 调用类 `owner` 中名称为 `name` ，描述符为 `desc` 的虚方法， `objectref` 为类的实例，如果返回值类型不为`void`则返回值入栈       |

# InvokeDynamic

| Opcode                                                 | Stack: [before]→[after]     | Description                      |
|--------------------------------------------------------|-----------------------------|----------------------------------|
| `invokedynamic` name, desc, bsm, bootstrap_arguments[] | [arg1, [arg2 ...]] → <结果> | 动态调用(`callsite`在运行时生成) |

# Jump

| Opcode            | Stack: [before]→[after] | Description                                  |
|-------------------|-------------------------|----------------------------------------------|
| `goto` label      | [no change]             | 跳转到 `label`                               |
| `if_acmpeq` label | 值1, 值2 →              | 如果 `值1` `值2` 引用相等 , 跳转到 `label`   |
| `if_acmpne` label | 值1, 值2 →              | 如果 `值1` `值2` 引用不相等 , 跳转到 `label` |
| `if_icmpeq` label | 值1, 值2 →              | 如果 两个`int` `值1 == 值2` , 跳转到 `label` |
| `if_icmpge` label | 值1, 值2 →              | 如果 两个`int` `值1 >= 值2` , 跳转到 `label` |
| `if_icmpgt` label | 值1, 值2 →              | 如果 两个`int` `值1 > 值2` , 跳转到 `label`  |
| `if_icmple` label | 值1, 值2 →              | 如果 两个`int` `值1 <= 值2` , 跳转到 `label` |
| `if_icmplt` label | 值1, 值2 →              | 如果 两个`int` `值1 < 值2` , 跳转到 `label`  |
| `if_icmpne` label | 值1, 值2 →              | 如果 两个`int` `值1 != 值2` , 跳转到 `label` |
| `ifeq` label      | 值 →                    | 如果 `值 == 0` , 跳转到 `label`              |
| `ifge` label      | 值 →                    | 如果 `值 >= 0` , 跳转到 `label`              |
| `ifgt` label      | 值 →                    | 如果 `值 > 0` , 跳转到 `label`               |
| `ifle` label      | 值 →                    | 如果 `值 <= 0` , 跳转到 `label`              |
| `iflt` label      | 值 →                    | 如果 `值 < 0` , 跳转到 `label`               |
| `ifne` label      | 值 →                    | 如果 `值 != 0` , 跳转到 `label`              |
| `ifnonnull` label | 值 →                    | 如果 `值 != null` , 跳转到 `label`           |
| `ifnull` label    | 值 →                    | 如果 `值 == null` , 跳转到 `label`           |

# Ldc

| Opcode   | Stack: [before]→[after] | Description                                                                                  |
|----------|-------------------------|----------------------------------------------------------------------------------------------|
| `ldc` 值 | → 值                    | 将一个常量 *( `String` , `int` , `float` , `long` , `double` , `Class` , or `Handle` )* 入栈 |

# Increment

| Opcode               | Stack: [before]→[after] | Description                                    |
|----------------------|-------------------------|------------------------------------------------|
| `iinc` <索引> amount | [No change]             | 将局部变量 `<索引>` 自增 `amount` *( `byte` )* |

# MultiANewArray

| Opcode                     | Stack: [before]→[after]            | Description                                                            |
|----------------------------|------------------------------------|------------------------------------------------------------------------|
| `multianewarray` desc dims | count1, [count2, ...] → <数组引用> | 创建一个 `dims` 维的数组，描述符为 `desc`；长度由`count1` `count2`等指定 |

# Switch

| Opcode         | Stack: [before]→[after] | Description                                 |
|----------------|-------------------------|---------------------------------------------|
| `lookupswitch` | key →                   | 通过 `key` 从非连续的表中查找目标地址并跳转 |
| `tableswitch`  | key →                   | 通过 `key` 从连续的表中查找目标地址并跳转   |

# Label

| Opcode  | Stack: [before]→[after] | Description                |
|---------|-------------------------|----------------------------|
| `label` | [No change]             | 标记一个label，ASM的伪指令。 |

# Line

| Opcode      | Stack: [before]→[after] | Description                              |
|-------------|-------------------------|------------------------------------------|
| `line` line | [No change]             | 标记接下来的字节码在源码里的行数为`line` |
