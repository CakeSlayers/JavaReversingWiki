# 前言

这里是被Java字节码库 *([ASM](https://asm.ow2.io/))* 简化过的Java字节指令码列表 . 这里的简明Java字节指令码是Recaf及其他字节码编辑/查看器采用的字节指令码标准[（官方字节指令码表）](https://docs.oracle.com/javase/specs/jvms/se12/html/jvms-6.html)

# 目录

[TOC]



# 指令

| 操作码         | 操作栈（按从栈底到栈顶的顺序排列）: [之前]→[之后]           | 描述                                                         |
| -------------- | ----------------------------------------------------------- | ------------------------------------------------------------ |
| `aconst_null`  | → `null`                                                    | `null` 值入栈                                                |
| `dconst_0`     | → `0.0`                                                     | 常量 `0.0` (double)值入栈                                    |
| `dconst_1`     | → `1.0`                                                     | 常量 `1.0` (double)值入栈                                    |
| `fconst_0`     | → `0.0f`                                                    | `0.0f`(float) 值入栈                                         |
| `fconst_1`     | → `1.0f`                                                    | `1.0f` (float)值入栈                                         |
| `fconst_2`     | → `2.0f`                                                    | `2.0f` (float)值入栈                                         |
| `iconst_m1`    | → `-1`                                                      | -1(int)值入栈                                                |
| `iconst_0`     | → `0`                                                       | 0(int)值入栈                                                 |
| `iconst_1`     | → `1`                                                       | 1(int)值入栈                                                 |
| `iconst_2`     | → `2`                                                       | 2(int)值入栈                                                 |
| `iconst_3`     | → `3`                                                       | 3(int)值入栈                                                 |
| `iconst_4`     | → `4`                                                       | 4(int)值入栈                                                 |
| `iconst_5`     | → `5`                                                       | 5(int)值入栈                                                 |
| `lconst_0`     | → `0L`                                                      | 0L(long)值入栈                                               |
| `lconst_1`     | → `1L`                                                      | 1L(long)值入栈                                               |
| `arraylength`  | <数组引用>→ <数组长度>                                      | 获取数组长度                                                 |
| `aaload`       | <数组引用>, <索引> → 值                                     | 从引用类型数组中入栈指定项的值                               |
| `aastore`      | <数组引用>, <索引>, 值 →                                    | 将栈顶引用类型值储存到指定引用类型数组的指定项               |
| `baload`       | <数组引用>, <索引> → 值                                     | 从`boolean`类型数组或`byte`类型数组中入栈指定项的值          |
| `bastore`      | <数组引用>, <索引>, 值 →                                    | 将栈顶`boolean`类型值或`byte`类型值储存到指定`boolean`类型数组或`byte`类型数组的指定项 |
| `caload`       | <数组引用>, <索引> → 值                                     | 将`char`型数组指定索引的值入栈                               |
| `castore`      | <数组引用>, <索引>, 值 →                                    | 将栈顶`char`类型值储存到对应类型数组的指定项                 |
| `daload`       | <数组引用>, <索引> → 值                                     | 将`double`型数组指定索引的值推送至栈顶                       |
| `dastore`      | <数组引用>, <索引>, 值 →                                    | 将栈顶`double` 类型值储存到对应类型数组的指定项              |
| `faload`       | <数组引用>, <索引> → 值                                     | load a `float` from an array                                 |
| `fastore`      | <数组引用>, <索引>, 值 →                                    | store a `float` in an array                                  |
| `iaload`       | <数组引用>, <索引> → 值                                     | load an `int` from an array                                  |
| `iastore`      | <数组引用>, <索引>, 值 →                                    | store an `int` into an array                                 |
| `laload`       | <数组引用>, <索引> → 值                                     | load a `long` from an array                                  |
| `lastore`      | <数组引用>, <索引>, 值 →                                    | store a `long` to an array                                   |
| `saload`       | <数组引用>, <索引> → 值                                     | load `short` from array                                      |
| `sastore`      | <数组引用>, <索引>, 值 →                                    | store `short` to array                                       |
| `d2f`          | 值 → <结果>                                                 | 类型转换: `double` 到 `float`                                |
| `d2i`          | 值 → <结果>                                                 | 类型转换: `double` 到 `int`                                  |
| `d2l`          | 值 → <结果>                                                 | 类型转换: `double` 到 `long`                                 |
| `f2d`          | 值 → <结果>                                                 | 类型转换: `float` 到 `double`                                |
| `f2i`          | 值 → <结果>                                                 | 类型转换: `float` 到 `int`                                   |
| `f2l`          | 值 → <结果>                                                 | 类型转换: `float` 到 `long`                                  |
| `i2b`          | 值 → <结果>                                                 | 类型转换: `int` 到 `byte`                                    |
| `i2c`          | 值 → <结果>                                                 | 类型转换: `int` 到 `char`                                    |
| `i2d`          | 值 → <结果>                                                 | 类型转换: `int` 到 `double`                                  |
| `i2f`          | 值 → <结果>                                                 | 类型转换: `int` 到 `float`                                   |
| `i2l`          | 值 → <结果>                                                 | 类型转换: `int` 到 `long`                                    |
| `i2s`          | 值 → <结果>                                                 | 类型转换: `int` 到 `short`                                   |
| `l2d`          | 值 → <结果>                                                 | 类型转换: `long` 到 `double`                                 |
| `l2f`          | 值 → <结果>                                                 | 类型转换: `long` 到 `float`                                  |
| `l2i`          | 值 → <结果>                                                 | 类型转换: `long` 到 `int`                                    |
| `areturn`      | 引用 → [堆栈销毁]                                           | 返回一个引用                                                 |
| `dreturn`      | 值 → [堆栈销毁]                                             | 返回一个 `double`                                            |
| `freturn`      | 值 → [堆栈销毁]                                             | 返回一个 `float`                                             |
| `ireturn`      | 值 → [堆栈销毁]                                             | 返回一个 `int`                                               |
| `lreturn`      | 值 → [堆栈销毁]                                             | 返回一个 `long`                                              |
| `return`       | → [堆栈销毁]                                                | 直接返回 (`void`)                                            |
| `dadd`         | 值1, 值2 → <结果>                                           | add two `double` 值s `值2 + 值1`                             |
| `ddiv`         | 值1, 值2 → <结果>                                           | divide two `double` 值s `值2 / 值1`                          |
| `dmul`         | 值1, 值2 → <结果>                                           | multiply two `double` 值s `值2 * 值1`                        |
| `drem`         | 值1, 值2 → <结果>                                           | get the remainder from a division between two `double` 值s `(值2 - ((值1 / 值2) * 值2))` |
| `dsub`         | 值1, 值2 → <结果>                                           | subtract a `double` from another `值2 - 值1`                 |
| `fadd`         | 值1, 值2 → <结果>                                           | add two `float` 值s `值2 + 值1`                              |
| `fdiv`         | 值1, 值2 → <结果>                                           | divide two `float` 值s `值2 / 值1`                           |
| `fmul`         | 值1, 值2 → <结果>                                           | multiply two `float` 值s `值2 * 值1`                         |
| `frem`         | 值1, 值2 → <结果>                                           | get the remainder from a division between two `float` 值s `(值2 - ((值1 / 值2) * 值2))` |
| `fsub`         | 值1, 值2 → <结果>                                           | subtract two `float` 值s `值2 - 值1`                         |
| `iadd`         | 值1, 值2 → <结果>                                           | add two `int` 值s `值2 + 值1`                                |
| `idiv`         | 值1, 值2 → <结果>                                           | divide two `int` 值s `值2 / 值1`                             |
| `imul`         | 值1, 值2 → <结果>                                           | multiply two `int` 值s `值2 * 值1`                           |
| `irem`         | 值1, 值2 → <结果>                                           | logical `int` remainder `(值2 - ((值1 / 值2) * 值2))`        |
| `isub`         | 值1, 值2 → <结果>                                           | `int` subtract `值2 - 值1`                                   |
| `iand`         | 值1, 值2 → <结果>                                           | perform a bitwise AND on two `int` 值s `值2 & 值1`           |
| `ior`          | 值1, 值2 → <结果>                                           | bitwise `int` OR `值2                                        |
| `ixor`         | 值1, 值2 → <结果>                                           | `int` xor `值2 ^ 值1`                                        |
| `ishl`         | 值1, 值2 → <结果>                                           | `int` shift left `值2 << 值1`                                |
| `ishr`         | 值1, 值2 → <结果>                                           | `int` arithmetic shift right `值2 >> 值1`                    |
| `iushr`        | 值1, 值2 → <结果>                                           | `int` logical shift right `值2 >>> 值1`                      |
| `ladd`         | 值1, 值2 → <结果>                                           | add two `long` 值s `值2 + 值1`                               |
| `ldiv`         | 值1, 值2 → <结果>                                           | divide two `long` 值s `值2 / 值1`                            |
| `lmul`         | 值1, 值2 → <结果>                                           | multiply two `long` 值s `值2 * 值1`                          |
| `lrem`         | 值1, 值2 → <结果>                                           | remainder of division of two `long` 值s `(值2 - ((值1 / 值2) * 值2))` |
| `lsub`         | 值1, 值2 → <结果>                                           | subtract two `long` 值s `值2 - 值1`                          |
| `lshl`         | 值1, 值2 → <结果>                                           | bitwise shift left of a `long` 值1 by `int` `值2` positions `值2 << 值1` |
| `lshr`         | 值1, 值2 → <结果>                                           | bitwise shift right of a `long` 值1 by `int` `值2` positions `值2 >> 值1` |
| `lushr`        | 值1, 值2 → <结果>                                           | bitwise shift right of a `long` 值1 by `int` `值2` positions, unsigned `值2 >>> 值1` |
| `land`         | 值1, 值2 → <结果>                                           | bitwise AND of two `long` 值s `值2 ^ 值1`                    |
| `lor`          | 值1, 值2 → <结果>                                           | bitwise OR of two `long` 值s `值2                            |
| `lxor`         | 值1, 值2 → <结果>                                           | bitwise XOR of two `long` 值s `值2 ^ 值1`                    |
| `dneg`         | 值 → <结果>                                                 | 取反 `double` `-值`                                          |
| `fneg`         | 值 → <结果>                                                 | 取反 `float` `-值`                                           |
| `ineg`         | 值 → <结果>                                                 | 取反 `int` `-值`                                             |
| `lneg`         | 值 → <结果>                                                 | 取反 `long` `-值`                                            |
| `dcmpg`        | 值1, 值2 → <结果>                                           | compare two `double` 值s ●Comparison值值1==NaN or 值2==NaN1值1 > 值21值1==值20值1 < 值2-1 |
| `dcmpl`        | 值1, 值2 → <结果>                                           | compare two `double` 值s ●Comparison值值1==NaN or 值2==NaN-1值1 > 值21值1==值20值1 < 值2-1 |
| `fcmpg`        | 值1, 值2 → <结果>                                           | compare two `float` 值s ●Comparison值值1==NaN or 值2==NaN1值1 > 值21值1==值20值1 < 值2-1 |
| `fcmpl`        | 值1, 值2 → <结果>                                           | compare two `float` 值s ●Comparison值值1==NaN or 值2==NaN-1值1 > 值21值1==值20值1 < 值2-1 |
| `lcmp`         | 值1, 值2 → <结果>                                           | compare two `long` 值s ●Comparison值值1==值20值1 > 值21else-1 |
| `athrow`       | objectref → [empty], objectref                              | throws an error or exception *(notice that the rest of the stack is cleared, leaving only a reference to the `Throwable`)* |
| `dup`          | 值 → 值, 值                                                 | duplicate the 值 on top of the stack                         |
| `dup_x1`       | 值2, 值1 → 值1, 值2, 值1                                    | insert a copy of the top 值 into the stack two 值s from the top. `值1` and `值2` must not be of the type `double` or `long`. |
| `dup_x2`       | 值3, 值2, 值1 → 值1, 值3, 值2, 值1                          | insert a copy of the top 值 into the stack two *(if `值2` is `double` or `long` it takes up the entry of `值3`, too)* or three 值s (if `值2` is neither `double` nor `long`) from the top |
| `dup2`         | {值2, 值1} → {值2, 值1}, {值2, 值1}                         | duplicate top two stack words *(two 值s, if `值1` is not `double` nor long; a single 值, if 值1 is `double` or `long`)* |
| `dup2_x1`      | 值3, {值2, 值1} → {值2, 值1}, 值3, {值2, 值1}               | duplicate two words and insert beneath third word *(see explanation above)* |
| `dup2_x2`      | {值4, 值3}, {值2, 值1} → {值2, 值1}, {值4, 值3}, {值2, 值1} | duplicate two words and insert beneath fourth word           |
| `pop`          | 值 →                                                        | discard the top 值 入栈                                      |
| `pop2`         | {值2, 值1} →                                                | discard the top two 值s 入栈 *(or one 值, if it is a `double` or long)* |
| `swap`         | 值2, 值1 → 值1, 值2                                         | swaps two top words 入栈 *(note that `值1` and `值2` must not be `double` or long)* |
| `monitorenter` | 引用 →                                                      | 进入同步块，获取对象的锁                                     |
| `monitorexit`  | 引用 →                                                      | 退出同步块，释放对象的锁                                     |
| `nop`          | [无变化]                                                    | 无操作                                                       |

# Integer

| Opcode                 | Stack: [before]→[after] | Description                                                  |
| ---------------------- | ----------------------- | ------------------------------------------------------------ |
| `bipush` ●值           | → 值                    | push a `byte` onto the stack as an `int` 值                  |
| `sipush` ●值           | → 值                    | push a `short` onto the stack as an `int` 值                 |
| `newarray` ●descriptor | count → <数组引用>      | create new array with count elements of primitive type identified by descriptor （类型描述符如下） |

|  类型   | 描述符缩写 |
| :-----: | :--------: |
| boolean |     Z      |
|  char   |     C      |
|  float  |     F      |
| double  |     D      |
|  byte   |     B      |
|  short  |     S      |
|   int   |     I      |
|  long   |     J      |



# Variable

| Opcode       | Stack: [before]→[after] | Description                                                  |
| ------------ | ----------------------- | ------------------------------------------------------------ |
| `iload` ●值  | → 值                    | load an `int` 值 from a local variable <索引>                |
| `lload` ●值  | → 值                    | load a `long` 值 from a local variable <索引>                |
| `fload` ●值  | → 值                    | load a `float` 值 from a local variable <索引>               |
| `dload` ●值  | → 值                    | load a `double` 值 from a local variable <索引>              |
| `aload` ●值  | → objectref             | load a reference onto the stack from a local variable <索引> |
| `istore` ●值 | 值 →                    | store `int` 值 into variable <索引>                          |
| `lstore` ●值 | 值 →                    | store a `long` 值 in a local variable <索引>                 |
| `fstore` ●值 | 值 →                    | store a `float` 值 into a local variable <索引>              |
| `dstore` ●值 | 值 →                    | store a `double` 值 into a local variable <索引>             |
| `astore` ●值 | objectref →             | store a reference into a local variable <索引>               |

# Type

| Opcode             | Stack: [before]→[after] | Description                                                  |
| ------------------ | ----------------------- | ------------------------------------------------------------ |
| `new` ●type        | → objectref             | create new object of `type`                                  |
| `anewarray` ●type  | count → <数组引用>      | create a new array of references of length `count` and component `type` identified by type |
| `checkcast` ●type  | objectref → objectref   | checks whether an `objectref` is of a certain specified `type` |
| `instanceof` ●type | objectref → <结果>      | determines if an object `objectref` is of a given `type`     |

# Field

| Opcode                     | Stack: [before]→[after] | Description                                                  |
| -------------------------- | ----------------------- | ------------------------------------------------------------ |
| `getfield` ●ownernamedesc  | objectref → 值          | get an instance field defined by the `owner` class and the field's `name` and `desc` |
| `getstatic` ●ownernamedesc | → 值                    | get a static field defined by the `owner` class and the field's `name` and `desc` |
| `putfield` ●ownernamedesc  | objectref, 值 →         | set an instance field defined by the `owner` class and the field's `name` and `desc` |
| `putstatic` ●ownernamedesc | 值 →                    | set a static field defined by the `owner` class and the field's `name` and `desc` |

# Method

| Opcode                           | Stack: [before]→[after]               | Description                                                  |
| -------------------------------- | ------------------------------------- | ------------------------------------------------------------ |
| `invokeinterface` ●ownernamedesc | objectref, [arg1, arg2, ...] → <结果> | invokes an interface method defined by the `owner` class and the method's `name` and `desc` on object `objectre`f and puts the <结果> 入栈 *(might be `void`)* |
| `invokespecial` ●ownernamedesc   | objectref, [arg1, arg2, ...] → <结果> | invokes an instance method defined by the `owner` class and the method's `name` and `desc` on object `objectref` and puts the <结果> 入栈 *(might be `void`)* |
| `invokestatic` ●ownernamedesc    | [arg1, arg2, ...] → <结果>            | invokes a static method defined by the `owner` class and the method's `name` and `desc` and puts the <结果> 入栈 *(might be `void`)* |
| `invokevirtual` ●ownernamedesc   | objectref, [arg1, arg2, ...] → <结果> | invokes a virtual method defined by the `owner` class and the method's `name` and `desc` on object `objectref` and puts the <结果> 入栈 *(might be `void`)* |

# InvokeDynamic

| Opcode                                                       | Stack: [before]→[after]   | Description                                                  |
| ------------------------------------------------------------ | ------------------------- | ------------------------------------------------------------ |
| `invokedynamic` ●definitionname, descbootstrap handleowner, name, descbootstrap arguments[] | [arg1, arg2 ...] → <结果> | invokes a dynamic method and puts the <结果> 入栈 *(might be `void`)*. The `callsite` handles the dynamic invocation. |

# Jump

| Opcode             | Stack: [before]→[after] | Description                                 |
| ------------------ | ----------------------- | ------------------------------------------- |
| `goto` ●label      | [no change]             | jump to `label`                             |
| `if_acmpeq` ●label | 值1, 值2 →              | if references `值1 == 值2`, jump to `label` |
| `if_acmpne` ●label | 值1, 值2 →              | if references `值1 != 值2`, jump to `label` |
| `if_icmpeq` ●label | 值1, 值2 →              | if ints `值1 == 值2`, jump to `label`       |
| `if_icmpge` ●label | 值1, 值2 →              | if ints `值1 >= 值2`, jump to `label`       |
| `if_icmpgt` ●label | 值1, 值2 →              | if ints `值1 > 值2`, jump to `label`        |
| `if_icmple` ●label | 值1, 值2 →              | if ints `值1 <= 值2`, jump to `label`       |
| `if_icmplt` ●label | 值1, 值2 →              | if ints `值1 < 值2`, jump to `label`        |
| `if_icmpne` ●label | 值1, 值2 →              | if ints `值1 != 值2`, jump to `label`       |
| `ifeq` ●label      | 值 →                    | if `值 == 0`, jump to `label`               |
| `ifge` ●label      | 值 →                    | if `值 >= 0`, jump to `label`               |
| `ifgt` ●label      | 值 →                    | if `值 > 0`, jump to `label`                |
| `ifle` ●label      | 值 →                    | if `值 <= 0`, jump to `label`               |
| `iflt` ●label      | 值 →                    | if `值 < 0`, jump to `label`                |
| `ifne` ●label      | 值 →                    | if `值 != 0`, jump to `label`               |
| `ifnonnull` ●label | 值 →                    | if `值 != null`, jump to `label`            |
| `ifnull` ●label    | 值 →                    | if `值 == null`, jump to `label`            |

# Ldc

| Opcode    | Stack: [before]→[after] | Description                                                  |
| --------- | ----------------------- | ------------------------------------------------------------ |
| `ldc` ●值 | → 值                    | push a constant 值 *(`String`, `int`, `float`, `long`, `double`, `Class`, or `Handle`)* onto the stack |

# Increment

| Opcode               | Stack: [before]→[after] | Description                                                  |
| -------------------- | ----------------------- | ------------------------------------------------------------ |
| `iinc` ●<索引>amount | [No change]             | increment local variable `<索引>` by a given `amount` *(`byte`)* |

# MultiANewArray

| Opcode                     | Stack: [before]→[after]           | Description                                                  |
| -------------------------- | --------------------------------- | ------------------------------------------------------------ |
| `multianewarray` ●descdims | count1, [count2,...] → <数组引用> | create a new array of `dims` dimensions of type identified by `desc` |

# Switch

| Opcode         | Stack: [before]→[after] | Description                                                  |
| -------------- | ----------------------- | ------------------------------------------------------------ |
| `lookupswitch` | key →                   | a target address is looked up from a table using a `key` and execution continues from the instruction at that address |
| `tableswitch`  | <索引> →                | continue execution from an address in the table at offset `<索引>` |

# Label

| Opcode  | Stack: [before]→[after] | Description                                                  |
| ------- | ----------------------- | ------------------------------------------------------------ |
| `label` | [No change]             | marker in bytecode for the beginning of a block of opcodes; referenced by jump and switch instructions. |

# Line

| Opcode       | Stack: [before]→[after] | Description                                                  |
| ------------ | ----------------------- | ------------------------------------------------------------ |
| `line` ●line | [No change]             | marker for where the next instruction denotes the beginning of a given line in the original source. |