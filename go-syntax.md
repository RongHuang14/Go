<img width="795" alt="image" src="https://github.com/user-attachments/assets/a488f124-f617-4338-bc35-f4edcd123f1c" />

<img width="658" alt="image" src="https://github.com/user-attachments/assets/b1cc2d10-a167-44a9-84b3-a68245e8c12c" />

# Golang Environment Setup （Golang环境安装）

# Golang Language Features （Golang语法特性）
<img width="909" alt="image" src="https://github.com/user-attachments/assets/056610f9-dd47-4250-9ba2-1e5896d7cc8c" />
<img width="902" alt="image" src="https://github.com/user-attachments/assets/915c1c34-9ec0-400f-b814-c7bd80de6573" />
<img width="923" alt="image" src="https://github.com/user-attachments/assets/644fb45e-b1bd-446d-8948-886ed6828691" />
<img width="928" alt="image" src="https://github.com/user-attachments/assets/a10c698a-8767-4645-b785-9245548c298c" />
<img width="928" alt="image" src="https://github.com/user-attachments/assets/9549876e-95a7-4551-9af7-7da79581266b" />
<img width="835" alt="image" src="https://github.com/user-attachments/assets/f1d98cf3-a27b-4678-8e2d-f4c86e43b07e" />
<img width="911" alt="image" src="https://github.com/user-attachments/assets/7b398a33-3388-4669-b673-71626a91bf75" />
<img width="825" alt="image" src="https://github.com/user-attachments/assets/86121229-47a3-458c-b817-6d9c227230a5" />


# Golang Syntax & Concepts (从一个main函数初见Golang语法)

## Understanding Golang Syntax from a Main Function (从一个main函数初见Golang语法)

### 1. Golang 基础结构
一个 Go 程序的基本组成：
```go
package main   // 指定程序的包名，必须是 main

import "fmt"   // 导入标准库 fmt

// main 函数 - Go 程序的入口
func main() {
    fmt.Println("Hello, World!") // 打印输出
}
```
 <img width="842" alt="image" src="https://github.com/user-attachments/assets/e1bb8148-f8cc-4dac-a88e-1b06fb8884c7" />

**常见格式化占位符：**
| 占位符 | 作用 | 示例 | 输出 |
|--------|------|------|------|
| `%T` | 输出变量的数据类型 | `fmt.Printf("%T", 42)` | `int` |
| `%s` | 输出字符串 | `fmt.Printf("%s", "hello")` | `hello` |
| `%d` | 输出十进制整数 | `fmt.Printf("%d", 42)` | `42` |
| `%f` | 输出浮点数 | `fmt.Printf("%.2f", 3.1415)` | `3.14` |
| `%v` | **通用占位符**（自动匹配类型） | `fmt.Printf("%v", 42.5)` | `42.5` |
| `%q` | 输出带双引号的字符串 | `fmt.Printf("%q", "hello")` | `"hello"` |

**示例代码：**
```go
package main
import "fmt"

func main() {
    var num int = 100
    var pi float64 = 3.1415
    var str string = "Golang"
    var boolean bool = true

    fmt.Printf("整数: %d
", num)       // 输出: 整数: 100
    fmt.Printf("浮点数: %.2f
", pi)    // 输出: 浮点数: 3.14
    fmt.Printf("字符串: %s
", str)     // 输出: 字符串: Golang
    fmt.Printf("布尔值: %v
", boolean) // 输出: 布尔值: true
    fmt.Printf("变量类型: %T
", pi)    // 输出: 变量类型: float64
}
```（package），用于格式化 I/O（输入输出），类似于 Python 里的 `print()`，C 语言的 `printf()`。
- `Println` 是 `fmt` 包中的一个函数，用于输出内容并**自动换行**。


### 2⃣ 运行 Go 代码
Go 代码可以通过以下两种方式运行：

#### **🔹 方法 1：`go run` （直接运行）**
```bash
go run hello.go
```
**特点**：
- 适用于**测试和临时运行**代码
- **不会生成可执行文件**

#### **🔹 方法 2：`go build` （编译成二进制）**
```bash
go build hello.go  # 编译生成可执行文件
ls                 # 查看文件列表
./hello            # 运行可执行文件
```
**特点**：
- **生成二进制文件**，适用于生产环境部署
- **运行速度更快**

<img width="627" alt="image" src="https://github.com/user-attachments/assets/08aafb72-6e45-45ee-86ab-bb8624c4c507" />

### 2. Go 语言基础语法
#### 行分割符
golang中的表达式加不加分号无所谓建议不加
<img width="471" alt="image" src="https://github.com/user-attachments/assets/065c15b9-4cd6-4833-8f6d-b2ad4d9f073d" />

#### 注释
单行注释：//
多行注释：/*  */
<img width="602" alt="image" src="https://github.com/user-attachments/assets/05c62559-20b9-482f-a890-b4361af10bfb" />

#### 标识符
标识符用来命名变量、类型等程序实体。一个标识符实际上就是一个或是多个字母(A~Z和a~z)数字(0~9)、下划线_组成的序列，但是第一个字符必须是字母或下划线而不能是数字。

以下是有效的标识符：
```bash
mahesh   kumar   abc   move_name   a_123
myname50   _temp   j   a23b9   retVal
```
以下是无效的标识符：
1ab（以数字开头）
case（Go 语言的关键字）
a+b（运算符是不允许的）

#### 字符串连接
<img width="607" alt="image" src="https://github.com/user-attachments/assets/53d61dc3-cf7a-4851-8999-55c8e0a32259" />

#### 关键字
<img width="848" alt="image" src="https://github.com/user-attachments/assets/58ed77d9-88f2-4b6b-8aa4-4161cccd2067" />

### 3. Go 语言数据类型
#### **基本数据类型**
| 类型 | 说明 |
|------|------|
| `bool` | 布尔型，值为 `true` 或 `false` |
| `int`, `float32`, `float64` | 整型和浮点型，支持复数，位运算采用补码 |
| `string` | 字符串，UTF-8 编码，存储 Unicode 文本 |

#### **派生类型**
| 类型 | 说明 |
|------|------|
| `Pointer` | 指针类型 |
| `Array` | 数组类型 |
| `struct` | 结构体类型 |
| `Channel` | 并发通信通道 |
| `Function` | 函数类型 |
| `Slice` | 切片类型（动态数组） |
| `interface` | 接口类型 |
| `Map` | 映射（键值对）类型 |

### 4. Go 语言变量

#### **变量的四种声明方式**
（全局变量只能使用方法 1、2、3，方法 4 仅限函数内部）
1. **方法一：声明变量但不初始化（默认零值）**
   ```go
   var a int
   fmt.Println(a) // 输出: 0
   ```

2. **方法二：声明变量并初始化**
   ```go
   var b int = 100
   fmt.Println(b) // 输出: 100
   ```

3. **方法三：省略类型，自动推导**
   ```go
   var c = "hello"
   fmt.Println(c) // 输出: hello
   ```
   
4. **方法四：使用 `:=` 省略 `var` 直接自动匹配（仅限函数内部）（常用的方法）**

```go
package main
import "fmt"

func main() {
    e := 100
    fmt.Println("e =", e)
    fmt.Printf("type of e = %T
", e)

    f := "abcd"
    fmt.Println("f =", f)
    fmt.Printf("type of f = %T
", f)

    g := 3.14
    fmt.Println("g =", g)
    fmt.Printf("type of g = %T
", g)
}
```

**预期输出：**
```
e = 100
type of e = int
f = abcd
type of f = string
g = 3.14
type of g = float64
```

- `:=` 只能用于函数内部，自动推导变量类型。



#### **零值概念**
- 变量未初始化时，会赋默认零值：
  ```go
  var s string
  var i int
  var b bool
  fmt.Println(s, i, b) // 输出: "" 0 false
  ```
  | 类型 | 零值 |
  |------|------|
  | `int` | 0 |
  | `float64` | 0.0 |
  | `bool` | false |
  | `string` | ""（空字符串） |
  | 指针、切片、map、通道 | `nil` |

#### **多变量声明**
- **同一行声明多个变量（类型相同或不同）**
  ```go
  var x, y int = 100, 200
  var a, b = 123, "hello"
  fmt.Println(x, y, a, b) // 输出: 100 200 123 hello
  ```

- **使用 `:=` 声明多个变量（仅限函数内）**
  ```go
  m, n := 10, 20
  fmt.Println(m, n) // 输出: 10 20
  ```

- **分组声明**
  ```go
  var (
      v1 int  = 100
      v2 bool = true
  )
  fmt.Println(v1, v2) // 输出: 100 true


#### **并行赋值**
- **变量交换**
  ```go
  a, b := 5, 7
  a, b = b, a
  fmt.Println(a, b) // 输出: 7 5
  ```
- **丢弃不需要的值**
  ```go
  _, value := 10, 20
  fmt.Println(value) // 输出: 20
  ```

### 5. Go 语言常量

在 Go 语言中，**常量（constant）** 指的是 **在程序运行期间不会改变的值**，使用 `const` 关键字声明。

#### **1️⃣ 单个常量声明**
```go
package main
import "fmt"

func main() {
    const length int = 10
    fmt.Println("length =", length) // 输出: length = 10

    // length = 100  // ❌ 错误: 常量不能被修改
}
```
- 常量必须在声明时初始化，**不能** 之后再赋值或修改。

#### **2️⃣ 多个常量声明**
```go
const (
    PI  = 3.14
    E   = 2.718
    MSG = "Hello, Go!"
)

func main() {
    fmt.Println(PI, E, MSG) // 输出: 3.14 2.718 Hello, Go!
}
```

#### **3️⃣ 枚举常量（iota 计数器）**
`iota` 是 Go 语言提供的 **常量生成器**，可以用来创建**连续递增的值**。

```go
const (
    A = iota  // 0
    B         // 1
    C         // 2
)

func main() {
    fmt.Println(A, B, C) // 输出: 0 1 2
}
```
- `iota` 默认从 `0` 开始，每定义一行常量，它的值 **自动加 1**。

#### **4️⃣ iota 进阶用法**
```go
const (
    X, Y = iota + 1, iota + 2  // X=1, Y=2 (iota=0)
    M, N                      // M=2, N=3 (iota=1)
    P, Q                      // P=3, Q=4 (iota=2)

    R, S = iota * 2, iota * 3 // R=6, S=9 (iota=3)
    T, U                      // T=8, U=12 (iota=4)
)

func main() {
    fmt.Println(X, Y, M, N, P, Q, R, S, T, U)
    // 输出: 1 2 2 3 3 4 6 9 8 12
}
```
- **`iota` 在 `const` 代码块中按行递增**，可配合计算生成复杂的常量值。

#### **5️⃣ iota 位运算示例**
可用于 **位掩码** 或 **位移枚举**：
```go
const (
    READ   = 1 << iota // 1 (0001)
    WRITE             // 2 (0010)
    EXECUTE           // 4 (0100)
    DELETE            // 8 (1000)
)

func main() {
    fmt.Println(READ, WRITE, EXECUTE, DELETE) // 输出: 1 2 4 8
}
```
- `1 << iota` 让常量以 **2 的幂递增**，适用于权限管理、状态标记等场景。

---

### 6. Go 语言运算符

Go 语言运算符与 C 语言类似，包含 **算术运算符、关系运算符、逻辑运算符、位运算符、赋值运算符** 以及 **其他运算符（& 取地址、* 指针变量）**。

---

### 1️⃣ **算术运算符**
| 运算符 | 描述 | 示例 | 结果 |
|--------|------|------|------|
| `+` | 相加 | `10 + 5` | `15` |
| `-` | 相减 | `10 - 5` | `5` |
| `*` | 相乘 | `10 * 5` | `50` |
| `/` | 相除 | `10 / 2` | `5` |
| `%` | 取余 | `10 % 3` | `1` |
| `++` | 自增 | `a++` | `a = a + 1` |
| `--` | 自减 | `a--` | `a = a - 1` |

---

### 2️⃣ **关系运算符**
| 运算符 | 描述 | 示例 | 结果 |
|--------|------|------|------|
| `==` | 是否相等 | `10 == 20` | `false` |
| `!=` | 是否不等 | `10 != 20` | `true` |
| `>`  | 是否大于 | `10 > 5` | `true` |
| `<`  | 是否小于 | `10 < 5` | `false` |
| `>=` | 是否大于等于 | `10 >= 10` | `true` |
| `<=` | 是否小于等于 | `10 <= 5` | `false` |


---

### 3️⃣ **逻辑运算符**
| 运算符 | 描述 | 示例 | 结果 |
|--------|------|------|------|
| `&&` | 逻辑 AND | `true && false` | `false` |
| `||` | 逻辑 OR | `true || false` | `true` |
| `!`  | 逻辑 NOT | `!true` | `false` |


---

### 4️⃣ **位运算符**
| 运算符 | 描述 | 示例 | 结果 |
|--------|------|------|------|
| `&` | 按位与 | `12 & 5` | `4` |
| `|` | 按位或 | `12 | 5` | `13` |
| `^` | 按位异或 | `12 ^ 5` | `9` |
| `<<` | 左移 | `3 << 2` | `12` |
| `>>` | 右移 | `12 >> 2` | `3` |

---


### 5️⃣ **其他运算符（指针 & 变量地址）**

| 运算符 | 描述 | 示例 | 结果 |
|--------|------|------|------|
| `&` | 取变量地址 | `&a` | 变量 `a` 的内存地址 |
| `*` | 指针变量 | `*ptr` | 指针 `ptr` 指向的值 |



---

📌 **总结：**
- Go 语言运算符与 C 语言类似，支持 **算术、关系、逻辑、位运算、赋值、指针操作**。
- **`&` 取地址，`*` 指针解引用**，类似 C 语言指针操作。
- **优先级：** `* / %` > `+ -` > `== !=` > `&&` > `||`。

### 7. Go 语言条件语句

Go 语言的 **条件语句** 用于控制程序流程，支持 `if`、`if...else`、`switch` 以及 `select` 语句。

---

### 1️⃣ **if 语句**
用于 **判断条件是否为 true**，如果成立则执行代码块。
```go
package main
import "fmt"

func main() {
    num := 10
    if num > 5 {
        fmt.Println("num 大于 5")
    }
}
```
**输出：**
```
num 大于 5
```

---

### 2️⃣ **if...else 语句**
`else` 语句在 `if` 条件不满足时执行。
```go
package main
import "fmt"

func main() {
    num := 3
    if num > 5 {
        fmt.Println("num 大于 5")
    } else {
        fmt.Println("num 小于或等于 5")
    }
}
```
**输出：**
```
num 小于或等于 5
```

---

### 3️⃣ **if...else if...else 语句**
多个条件分支判断。
```go
package main
import "fmt"

func main() {
    num := 7
    if num > 10 {
        fmt.Println("num 大于 10")
    } else if num > 5 {
        fmt.Println("num 介于 6 到 10 之间")
    } else {
        fmt.Println("num 小于或等于 5")
    }
}
```
**输出：**
```
num 介于 6 到 10 之间
```

---

### 4️⃣ **switch 语句**
类似 `if...else`，但更简洁。
```go
package main
import "fmt"

func main() {
    day := 3
    switch day {
    case 1:
        fmt.Println("星期一")
    case 2:
        fmt.Println("星期二")
    case 3:
        fmt.Println("星期三")
    default:
        fmt.Println("未知日期")
    }
}
```
**输出：**
```
星期三
```

📌 **Go 的 switch 语句特点：**
- **无需 `break`**，匹配成功后默认不会继续执行。
- 使用 `fallthrough` 可强制执行下一个 case 代码。
- case 可以匹配多个值，如 `case 1, 2, 3:`。

---

### 5️⃣ **select 语句（用于通道并发）**
`select` 语句用于 **多通道通信**，随机选择可运行的 `case`。
```go
package main
import "fmt"
import "time"

func main() {
    ch1 := make(chan string, 1)
    ch2 := make(chan string, 1)
    
    go func() {
        time.Sleep(2 * time.Second)
        ch1 <- "来自 ch1"
    }()
    
    go func() {
        time.Sleep(1 * time.Second)
        ch2 <- "来自 ch2"
    }()
    
    select {
    case msg := <-ch1:
        fmt.Println("接收：", msg)
    case msg := <-ch2:
        fmt.Println("接收：", msg)
    }
}
```
📌 **`select` 语句特点：**
- **随机执行一个可运行的 `case`**。
- **如果没有 `case` 可运行，则阻塞，直到有 `case` 可执行**。

---

📢 **Go 语言不支持 `?:` 三目运算符**，只能使用 `if...else`。


### 8. Go 语言循环语句

Go 语言支持 `for` 关键字进行循环，提供 **普通循环、无限循环、循环控制语句**。

---

### 1️⃣ **基本 for 循环**
Go 语言 **仅支持 `for`** 作为循环关键字，没有 `while` 和 `do...while`。
```go
package main
import "fmt"

func main() {
    for i := 0; i < 5; i++ {
        fmt.Println("当前值：", i)
    }
}
```
**输出：**
```
当前值： 0
当前值： 1
当前值： 2
当前值： 3
当前值： 4
```

---

### 2️⃣ **省略初始语句和递增语句**
`for` 允许省略 **初始化** 和 **递增** 部分。
```go
package main
import "fmt"

func main() {
    i := 0
    for i < 5 {
        fmt.Println("当前值：", i)
        i++
    }
}
```
**输出：**
```
当前值： 0
当前值： 1
当前值： 2
当前值： 3
当前值： 4
```

---

### 3️⃣ **无限循环**
Go 语言的 `for` 语句 **可以没有任何条件**，形成无限循环。
```go
package main
import "fmt"

func main() {
    for {
        fmt.Println("无限循环")
    }
}
```
🔹 **注意：** 无限循环需配合 `break` 退出，否则会死循环。

---

### 4️⃣ **循环控制语句**
#### **`break` 语句（跳出循环）**
```go
package main
import "fmt"

func main() {
    for i := 0; i < 10; i++ {
        if i == 5 {
            break
        }
        fmt.Println("i =", i)
    }
}
```
**输出：**
```
i = 0
i = 1
i = 2
i = 3
i = 4
```

#### **`continue` 语句（跳过当前循环，继续下一次）**
```go
package main
import "fmt"

func main() {
    for i := 0; i < 5; i++ {
        if i == 2 {
            continue
        }
        fmt.Println("i =", i)
    }
}
```
**输出：**
```
i = 0
i = 1
i = 3
i = 4
```
🔹 **当 `i == 2` 时，`continue` 让程序跳过 `fmt.Println`，直接进入下一次循环。**

#### **`goto` 语句（跳转到指定标签）**
```go
package main
import "fmt"

func main() {
    i := 0
START:
    fmt.Println("i =", i)
    i++
    if i < 3 {
        goto START
    }
}
```
**输出：**
```
i = 0
i = 1
i = 2
```
🔹 **`goto` 不建议滥用，否则代码可读性会变差。**

---

📢 **Go 语言循环特点：**
- `for` 是唯一的循环语句（没有 `while` 和 `do...while`）。
- `for` 语句可以省略初始值、条件表达式、递增语句。
- 支持 `break`、`continue`、`goto` 进行循环控制。
  
### 9. Go 语言函数

Go 语言的 **函数** 是代码逻辑的基本单元，支持 **单返回值、多返回值（匿名/命名）、值传递与引用传递**。

---

### 1️⃣ **函数的基本定义**
**Go 语言函数格式：**
```go
func function_name([参数列表]) [返回类型] {
    函数体
}
```
📌 **解析：**
- `func`：声明函数的关键字。
- `function_name`：函数名称。
- `参数列表`：参数类型、顺序、个数。
- `返回类型`（可选）：指定返回值类型。

**示例：单返回值函数**
```go
package main
import "fmt"

func foo1(a string, b int) int {
    fmt.Println("a =", a)
    fmt.Println("b =", b)
    c := 100
    return c
}

func main() {
    c := foo1("abc", 555)
    fmt.Println("c =", c)
}
```
**输出：**
```
a = abc
b = 555
c = 100
```

---

### 2️⃣ **多个返回值**
#### **匿名返回值**
```go
package main
import "fmt"

func foo2(a string, b int) (int, int) {
    fmt.Println("a =", a)
    fmt.Println("b =", b)
    return 666, 777
}

func main() {
    ret1, ret2 := foo2("haha", 999)
    fmt.Println("ret1 =", ret1, "ret2 =", ret2)
}
```
**输出：**
```
a = haha
b = 999
ret1 = 666 ret2 = 777
```

#### **命名返回值**
```go
package main
import "fmt"

func foo3(a string, b int) (r1 int, r2 int) {
    fmt.Println("---- foo3 ----")
    fmt.Println("a =", a)
    fmt.Println("b =", b)
    
    // r1, r2 属于 foo3 的形参，作用域在整个函数体内。
    // 它们的初始值是 0（int 类型的默认零值）。
    fmt.Println("r1 =", r1)
    fmt.Println("r2 =", r2)
    
    // 给命名返回值赋值
    r1 = 1000
    r2 = 2000
    return
}

func main() {
    ret1, ret2 := foo3("foo3", 333)
    fmt.Println("ret1 =", ret1, "ret2 =", ret2)
}
```
**输出：**
```
---- foo3 ----
a = foo3
b = 333
r1 = 0
r2 = 0
ret1 = 1000 ret2 = 2000
```

#### **命名返回值（多个返回值类型相同，可省略类型声明）**
```go
package main
import "fmt"

func foo4(a string, b int) (r1, r2 int) {
    fmt.Println("---- foo4 ----")
    fmt.Println("a =", a)
    fmt.Println("b =", b)
    r1 = 1000
    r2 = 2000
    return
}

func main() {
    ret1, ret2 := foo4("foo4", 444)
    fmt.Println("ret1 =", ret1, "ret2 =", ret2)
}
```
**输出：**
```
---- foo4 ----
a = foo4
b = 444
ret1 = 1000 ret2 = 2000
```

---

### 3️⃣ **函数参数的传递**
#### **值传递**（默认方式）
- 传递的是 **变量副本**，不会影响原始值。
```go
package main
import "fmt"

func modifyVal(a int) {
    a = 100
}

func main() {
    x := 10
    modifyVal(x)
    fmt.Println("x =", x) // x 仍然是 10
}
```

#### **引用传递**（传递指针）
- 传递的是 **变量地址**，会影响原始值。
```go
package main
import "fmt"

func modifyPtr(a *int) {
    *a = 100
}

func main() {
    x := 10
    modifyPtr(&x)
    fmt.Println("x =", x) // x 变为 100
}
```

---

📌 **Go 语言函数特点：**
- **支持多个返回值。**
- **默认值传递，可使用指针实现引用传递。**
- **支持匿名函数、闭包、方法（带接收者）。**

✅ 这样总结是否清晰？🚀


### 10. Go 语言变量作用域

Go 语言中的 **变量作用域** 决定了变量的可见性和生命周期。变量可声明在：
- **局部作用域**（函数内）
- **全局作用域**（函数外）
- **形式参数作用域**（函数参数）

---

### 1️⃣ **局部变量**
- **函数体内** 声明的变量。
- **仅在函数内部可用**，参数和返回值变量也属于局部变量。

```go
package main
import "fmt"

func main() {
    var a, b, c int // 局部变量
    a, b = 10, 20
    c = a + b
    fmt.Printf("局部变量: a = %d, b = %d, c = %d\n", a, b, c)
}
```
**输出：**
```
局部变量: a = 10, b = 20, c = 30
```

---

### 2️⃣ **全局变量**
- **函数体外** 声明，**可在整个包内使用**。
- 如果被 **导出（首字母大写）**，可供其他包访问。

```go
package main
import "fmt"

var g int // 全局变量

func main() {
    var a, b int = 10, 20
    g = a + b // 全局变量赋值
    fmt.Printf("全局变量: a = %d, b = %d, g = %d\n", a, b, g)
}
```
**输出：**
```
全局变量: a = 10, b = 20, g = 30
```

📌 **注意：局部变量优先级高于全局变量**
```go
package main
import "fmt"

var g int = 20 // 全局变量

func main() {
    var g int = 10 // 局部变量，覆盖全局变量
    fmt.Printf("g = %d\n", g)
}
```
**输出：**
```
g = 10
```

---

### 3️⃣ **形式参数（函数参数）**
- **函数参数也是局部变量**，在函数作用域内有效。

```go
package main
import "fmt"

var a int = 20 // 全局变量

func main() {
    var a int = 10 // 局部变量
    var b int = 20
    fmt.Printf("main()函数中 a = %d\n", a)
    c := sum(a, b)
    fmt.Printf("main()函数中 c = %d\n", c)
}

func sum(a, b int) int { // 形式参数
    fmt.Printf("sum()函数中 a = %d\n", a)
    fmt.Printf("sum()函数中 b = %d\n", b)
    return a + b
}
```
**输出：**
```
main()函数中 a = 10
sum()函数中 a = 10
sum()函数中 b = 20
main()函数中 c = 30
```

📌 **变量作用范围总结：**
| 作用域 | 声明位置 | 可用范围 |
|--------|--------|--------|
| **局部变量** | 函数内 | 仅限该函数 |
| **全局变量** | 函数外 | 整个包，或导出供其他包使用 |
| **形式参数** | 函数参数 | 仅限该函数 |


### 11. Go 语言 `init` 函数与导包

在 Go 语言中，`init` 函数用于**初始化包**，主要作用如下：
- **在 `main()` 之前执行**，用于执行初始化逻辑。
- **一个包可以有多个 `init` 函数**（可以在同一个文件或多个文件中）。
- **`init` 不能被手动调用**，它会在包被导入时自动执行。

---
<img width="593" alt="image" src="https://github.com/user-attachments/assets/06bb384a-64ca-407c-847a-09e33d940bc7" />
<img width="635" alt="image" src="https://github.com/user-attachments/assets/6dbb7304-50d2-4c5a-9d78-3e327350e123" />


### 1️⃣ **`init` 函数示例**
```go
package lib1

import "fmt"

// 当前 lib1 包提供的 API，函数首字母需要大写表示是对外开放的。
func Lib1Test() {
    fmt.Println("lib1Test()...")
}

// `init` 在包导入时自动执行。
func init() {
    fmt.Println("lib1. init() ...")
}
```

```go
package lib2

import "fmt"

// 当前 lib2 包提供的 API，函数首字母需要大写表示是对外开放的。
func Lib2Test() {
    fmt.Println("lib2Test()...")
}

func init() {
    fmt.Println("lib2. init() ...")
}
```

```go
package main

import (
    "GolangStudy/5-init/lib1"
    "GolangStudy/5-init/lib2"
)

func main() {
    lib1.Lib1Test()
    lib2.Lib2Test()
}
```

**执行顺序：**
```
lib1. init() ...
lib2. init() ...
lib1Test()...
lib2Test()...
```
📌 **执行顺序解析**：
- `init()` 先执行（按 `import` 依赖顺序，从 `pkg3` 开始）。
- `main()` 最后执行。

---

### 2️⃣ **三种 `import` 导包方式**

Go 语言提供了三种 `import` 方式：

#### **1. 匿名导入（`_ "包路径"`）**
- 仅执行 `init()`，不会导出 API。
- 适用于只需要初始化某个包但不直接调用它的方法。

```go
import _ "GolangStudy/5-init/lib1"
```
📌 **适用场景**：
- 数据库驱动、日志系统等 **只需要 `init` 逻辑** 的情况。

---

#### **2. 别名导入（`别名 "包路径"`）**
- 给 `import` 进来的包起一个别名，调用时使用别名。

```go
import mylib2 "GolangStudy/5-init/lib2"

func main() {
    mylib2.Lib2Test() // 通过别名 `mylib2` 访问 `lib2`
}
```
📌 **适用场景**：
- 避免包名冲突，或**简化代码**（如 `fmt.Println()` → `f.Println()`）。

---

#### **3. 直接导入 `.`（不推荐）**
- 直接导入 `lib2` 的全部方法到当前作用域，无需包名前缀。

```go
import . "GolangStudy/5-init/lib2"

func main() {
    Lib2Test() // 直接调用 `lib2` 的 `Lib2Test()` 方法
}
```
📌 **缺点**：
- **可能导致命名冲突**，不利于代码可读性。
- **通常不推荐使用**，除非在测试代码或 `main` 包中。

---

### 3️⃣ **`import` 执行顺序示意图**

当 `main.go` 依赖 `lib1`，`lib1` 依赖 `lib2`，那么 `init()` 的执行顺序如下：

```
lib2. init() ...
lib1. init() ...
main() 执行
```

📌 **执行顺序总结**：
1. **先初始化 `lib2`（最底层依赖）。**
2. **再初始化 `lib1`（依赖 `lib2`）。**
3. **最后执行 `main()`。**

---

### 4️⃣ **总结**
✅ `init()` 在 `main()` 之前自动执行。
✅ `import _ "包路径"` 只执行 `init()`，不暴露 API。
✅ `import 别名 "包路径"` 用别名访问包，避免冲突。
✅ `import . "包路径"` 直接导入，不推荐使用。
✅ `init()` 执行顺序 **从最底层包开始**，按依赖层级递归执行。

🚀 **最佳实践**：
- **尽量避免使用 `import .`，推荐使用 `别名导入`。**
- **只在必要时使用 `init()`，避免隐藏逻辑导致调试困难。**


### 12. Go 语言指针
值传递
<img width="969" alt="image" src="https://github.com/user-attachments/assets/5b0be3cc-f8ca-48fc-8c4e-18cbd0f24221" />

引用传递
<img width="910" alt="image" src="https://github.com/user-attachments/assets/a365d6c0-e4f8-4373-a5a4-871d2abda243" />
在 Go 语言中，指针（Pointer） 是一个存储变量内存地址的变量。指针的主要作用是：

允许间接访问变量的值，可以修改函数外部的变量（引用传递）。

减少内存占用，避免大对象的值拷贝，提高程序效率。

在数据结构（链表、树等）和系统编程中广泛应用。

---


### 1️⃣ ** 值传递 vs. 引用传递 **
值传递：函数参数是变量的拷贝，函数内部修改不会影响原变量。
引用传递（指针）：函数参数是变量的地址，函数内部修改会影响原变量。
<img width="593" alt="image" src="https://github.com/user-attachments/assets/06bb384a-64ca-407c-847a-09e33d940bc7" />
<img width="635" alt="image" src="https://github.com/user-attachments/assets/6dbb7304-50d2-4c5a-9d78-3e327350e123" />


### 2️⃣ ** 指针的基本使用**

Go 语言提供了三种 `import` 方式：

#### **1. 取变量地址（&）**
Go 语言的 & 取地址符 可获取变量的内存地址：

```go
package main
import "fmt"

func main() {
    var a int = 10
    fmt.Printf("a 变量的地址: %p\n", &a)  // 输出变量 a 的内存地址
}
```
---

#### **2. 声明指针变量（*）**
- 指针变量存储的是变量的内存地址。

- 通过 * 访问指针所指向的值。

```go
package main
import "fmt"

func main() {
    var a int = 10
    var p *int  // 声明指针变量
    p = &a      // p 存储变量 a 的地址
    
    fmt.Printf("a 变量的地址: %p\n", &a)
    fmt.Printf("p 存储的地址: %p\n", p)
    fmt.Printf("p 指向的值: %d\n", *p) // 通过指针访问变量值
}
```

```go
a 变量的地址: 0xc0000140a0
p 存储的地址: 0xc0000140a0
p 指向的值: 10
```

---

#### **3. 指针作为函数参数（引用传递）**


### 1️⃣ **1. 值传递（不会修改原值）**

```
package main
import "fmt"

func swap(a int, b int) {
    temp := a
    a = b
    b = temp
}

func main() {
    a, b := 10, 20
    swap(a, b)
    fmt.Println("a =", a, "b =", b)  // 仍然是 10, 20
}
```

### 2️⃣ **指针传递（可以修改原值）**

```
package main
import "fmt"

func swap(pa *int, pb *int) {
    temp := *pa
    *pa = *pb
    *pb = temp
}

func main() {
    a, b := 10, 20
    swap(&a, &b)  // 传递指针
    fmt.Println("a =", a, "b =", b)  // 交换成功
}
```
输出：

```
a = 20 b = 10
```
📌 总结：

- 值传递：拷贝变量，不影响原值。

- 指针传递：传递变量地址，修改影响原值。

### 4️⃣ **指针的进阶使用**
1. 指针的默认值 nil
```
var p *int  // 指针默认值是 nil
fmt.Println(p == nil) // 输出: true
```
2. 指针的指针（二级指针）
```
package main
import "fmt"

func main() {
    var a int = 10
    var p *int = &a  // p 存储 a 的地址
    var pp **int = &p  // pp 存储 p 的地址
    
    fmt.Println("a =", a)
    fmt.Println("p 指向的值 =", *p)
    fmt.Println("pp 指向的值 =", **pp)
}
```
输出：
```
a = 10
p 指向的值 = 10
pp 指向的值 = 10
```

📌 总结：

- p 是一级指针，存储 a 的地址。

- pp 是二级指针，存储 p 的地址，可通过 **pp 访问 a 的值。

### 5️⃣ **总结**

✅ & 取地址符：获取变量的内存地址。
✅ * 指针运算符：访问指针所指向的值。
✅ 指针可以作为函数参数，实现引用传递。
✅ 默认值是 nil，避免 nil 指针错误。
✅ 支持二级指针（指向指针的指针）。

### 13. Go 语言 `defer` 语句

在 Go 语言中，`defer` 语句用于 **延迟执行某个函数**，通常用于：
- **确保资源释放（如文件关闭、解锁互斥锁等）**。
- **执行收尾逻辑（如日志记录、错误处理等）**。
- **配合 `return` 使用，确保返回值计算后再执行某些清理操作**。

---

#### 📌 **`defer` 语句执行顺序**
`defer` 语句 **按 **后进先出（LIFO）** 顺序执行，即先 `defer` 的函数最后执行，最后 `defer` 的函数最先执行。

#### **🔹 执行流程**
<img width="807" alt="image" src="https://github.com/user-attachments/assets/d610a1dd-7cd2-4f67-ba29-6769f9dcf31b" />

**示例**
```go
package main
import "fmt"

func main() {
    defer fmt.Println("defer 1")
    defer fmt.Println("defer 2")
    defer fmt.Println("defer 3")

    fmt.Println("Main function executed")
}
```

**输出**
```
Main function executed
defer 3
defer 2
defer 1
```

---

### 1️⃣ `defer` 和 `return` 谁先执行？

`defer` 语句会 **在 `return` 语句执行后，函数返回前执行**，示例如下：

```go
package main
import "fmt"

func returnAndDefer() int {
    defer fmt.Println("defer 执行...")
    fmt.Println("return 执行...")
    return 0
}

func main() {
    returnAndDefer()
}
```

**输出**
```
return 执行...
defer 执行...
```

📌 **总结**
- `return` 语句先计算返回值
- `defer` 语句在 `return` 之后执行

---

### 2️⃣ `defer` 的应用场景

- **文件操作**
  ```go
  file, err := os.Open("test.txt")
  if err != nil {
      log.Fatal(err)
  }
  defer file.Close()  // 确保文件最终被关闭
  ```
- **互斥锁**
  ```go
  mu.Lock()
  defer mu.Unlock()  // 确保锁最终释放
  ```
- **数据库连接**
  ```go
  db, err := sql.Open("mysql", dsn)
  defer db.Close()  // 确保数据库连接关闭
  ```

---

### 3️⃣ `defer` 关键点总结
✅ `defer` 采用 **后进先出（LIFO）** 规则执行  
✅ `defer` 在 **`return` 执行后，函数退出前** 运行  
✅ 适用于 **资源释放、错误处理、日志记录** 等场景  

### 14. Go 语言数组与 Slice

Go 语言提供了数组类型的数据结构。

数组是具有相同唯一类型的一组已编号且长度固定的数据项序列，这种类型可以是任意的原始类型例如整型、字符串或者自定义类型。

相对于去声明 `number0, number1, ..., number99` 的变量，使用数组形式 `numbers[0], numbers[1] ..., numbers[99]` 更加方便且易于扩展。

数组元素可以通过索引（位置）来读取（或者修改），索引从 `0` 开始，第一个元素索引为 `0`，第二个索引为 `1`，以此类推。

---

### 1️⃣ **声明数组**

Go 语言数组声明需要指定元素类型及元素个数，语法格式如下：

```go
var arrayName [size]dataType
```

其中：
- `arrayName` 是数组的名称。
- `size` 是数组的大小。
- `dataType` 是数组中元素的数据类型。

示例：

```go
var balance [10]float32
```

### 2️⃣ **初始化数组**

```go
var numbers = [5]int{1, 2, 3, 4, 5}
numbers := [5]int{1, 2, 3, 4, 5}
```

如果数组长度不确定，可以使用 `...` 代替数组的长度：

```go
balance := [...]float32{1000.0, 2.0, 3.4, 7.0, 50.0}
```

可以指定索引进行初始化：

```go
balance := [5]float32{1: 2.0, 3: 7.0}
```

---

### 3️⃣ **访问数组元素**

数组元素可以通过索引（位置）来读取。

```go
var salary float32 = balance[2]
```

完整实例：

```go
package main

import "fmt"

func main() {
   var n [10]int 
   var i int

   for i = 0; i < 10; i++ {
      n[i] = i + 100
   }

   for i = 0; i < 10; i++ {
      fmt.Printf("Element[%d] = %d\n", i, n[i])
   }
}
```

---

### 4️⃣ **数组作为参数（值传递）**

```go
package main

import "fmt"

func printArray(myArray [4]int) {
    for index, value := range myArray {
        fmt.Println("index =", index, ", value =", value)
    }
    myArray[0] = 111 // 修改不会影响原数组
}

func main() {
    myArray := [4]int{11, 22, 33, 44}
    printArray(myArray)
    fmt.Println(myArray) // 依旧是原值
}
```

---

### 5️⃣ **Slice（切片）**

切片是对数组的抽象，比数组更灵活。

```go
mySlice := []int{1, 2, 3, 4}
fmt.Printf("mySlice type is %T\n", mySlice)
```

切片是引用类型，传递时是**引用传递**：

```go
package main

import "fmt"

func modifySlice(slice []int) {
    slice[0] = 100 // 影响原切片
}

func main() {
    mySlice := []int{1, 2, 3, 4}
    modifySlice(mySlice)
    fmt.Println(mySlice) // [100, 2, 3, 4]
}
```

---

### 6️⃣ **切片的扩容机制**

```go
package main

import "fmt"

func main() {
    var numbers = make([]int, 3, 5)
    fmt.Printf("len = %d, cap = %d, slice = %v\n", len(numbers), cap(numbers), numbers)

    numbers = append(numbers, 1)
    fmt.Printf("len = %d, cap = %d, slice = %v\n", len(numbers), cap(numbers), numbers)

    numbers = append(numbers, 2)
    fmt.Printf("len = %d, cap = %d, slice = %v\n", len(numbers), cap(numbers), numbers)

    numbers = append(numbers, 3)
    fmt.Printf("len = %d, cap = %d, slice = %v\n", len(numbers), cap(numbers), numbers)
}
```

📌 **总结：**
- 数组是**固定大小**的，传递是值传递。
- `slice`（切片）是**动态的**，传递是引用传递。
- `append()` 超过容量时，容量会**翻倍增长**。


### 15. Go 语言 Map(集合)

Map 是一种无序的键值对的集合。

Map 最重要的一点是通过 key 来快速检索数据，key 类似于索引，指向数据的值。

Map 是一种集合，所以我们可以像迭代数组和切片那样迭代它。不过，Map 是无序的，遍历 Map 时返回的键值对的顺序是不确定的。

在获取 Map 的值时，如果键不存在，返回该类型的零值，例如 int 类型的零值是 0，string 类型的零值是 ""。

Map 是引用类型，如果将一个 Map 传递给一个函数或赋值给另一个变量，它们都指向同一个底层数据结构，因此对 Map 的修改会影响到所有引用它的变量。

---

### 1️⃣ 定义 Map

可以使用内建函数 `make` 或使用 `map` 关键字来定义 Map:

```go
// 使用 make 函数
map_variable := make(map[KeyType]ValueType, initialCapacity)
```

其中 `KeyType` 是键的类型，`ValueType` 是值的类型，`initialCapacity` 是可选的参数，用于指定 Map 的初始容量。

实例：

```go
// 创建一个空的 Map
m := make(map[string]int)

// 创建一个初始容量为 10 的 Map
m := make(map[string]int, 10)
```

也可以使用字面量创建 Map：

```go
// 使用字面量创建 Map
m := map[string]int{
    "apple":  1,
    "banana": 2,
    "orange": 3,
}
```

---

### 2️⃣ **操作 Map**

#### **获取元素**

```go
// 获取键值对
v1 := m["apple"]
v2, ok := m["pear"]  // 如果键不存在，ok 的值为 false，v2 的值为该类型的零值
```

#### **修改元素**

```go
// 修改键值对
m["apple"] = 5
```

#### **获取 Map 的长度**

```go
// 获取 Map 的长度
len := len(m)
```

#### **遍历 Map**

```go
// 遍历 Map
for k, v := range m {
    fmt.Printf("key=%s, value=%d\n", k, v)
}
```

#### **删除元素**

```go
// 删除键值对
delete(m, "banana")
```

---

### 3️⃣ **Map 使用示例**

#### **实例 1：基本操作**

```go
package main

import "fmt"

func main() {
    var siteMap map[string]string 
    siteMap = make(map[string]string)

    siteMap["Google"] = "谷歌"
    siteMap["Runoob"] = "菜鸟教程"
    siteMap["Baidu"] = "百度"
    siteMap["Wiki"] = "维基百科"

    for site := range siteMap {
        fmt.Println(site, "首都是", siteMap[site])
    }

    name, ok := siteMap["Facebook"]
    if ok {
        fmt.Println("Facebook 的站点是", name)
    } else {
        fmt.Println("Facebook 站点不存在")
    }
}
```

#### **实例 2：`delete()` 函数**

```go
package main

import "fmt"

func main() {
    countryCapitalMap := map[string]string{
        "France": "Paris", 
        "Italy": "Rome", 
        "Japan": "Tokyo", 
        "India": "New Delhi",
    }

    fmt.Println("原始地图")
    for country := range countryCapitalMap {
        fmt.Println(country, "首都是", countryCapitalMap[country])
    }

    delete(countryCapitalMap, "France")
    fmt.Println("法国条目被删除")

    fmt.Println("删除元素后地图")
    for country := range countryCapitalMap {
        fmt.Println(country, "首都是", countryCapitalMap[country])
    }
}
```

#### **实例 3：Map 引用传递**

```go
package main

import "fmt"

func printMap(cityMap map[string]string) {
    for key, value := range cityMap {
        fmt.Println("key = ", key)
        fmt.Println("value = ", value)
    }
}

func ChangeValue(cityMap map[string]string) {
    cityMap["England"] = "London"
}

func main() {
    cityMap := make(map[string]string)
    cityMap["China"] = "Beijing"
    cityMap["Japan"] = "Tokyo"
    cityMap["USA"] = "New York"

    printMap(cityMap)

    delete(cityMap, "China")
    cityMap["USA"] = "DC"
    ChangeValue(cityMap)

    fmt.Println("-------")
    printMap(cityMap)
}
```

# 16. Go 语言结构体

Go 语言中数组可以存储同一类型的数据，但在结构体中我们可以为不同项定义不同的数据类型。

结构体是由一系列具有相同类型或不同类型的数据构成的数据集合。

结构体表示一项记录，比如保存图书馆的书籍记录，每本书有以下属性：

- **Title** ：标题  
- **Author** ： 作者  
- **Subject**：学科  
- **ID**：书籍ID  

---

## 定义结构体

结构体定义需要使用 `type` 和 `struct` 语句。`struct` 语句定义一个新的数据类型，结构体中有一个或多个成员。`type` 语句设定了结构体的名称。

```go
type Books struct {
   title   string
   author  string
   subject string
   book_id int
}
```
一旦定义了结构体类型，它就能用于变量的声明，语法格式如下：

```go
variable_name := structure_variable_type {value1, value2...valuen}
```

或

```go
variable_name := structure_variable_type { key1: value1, key2: value2..., keyn: valuen}
```

示例：

```go
package main

import "fmt"

type Books struct {
   title   string
   author  string
   subject string
   book_id int
}

func main() {
    fmt.Println(Books{"Go 语言", "www.runoob.com", "Go 语言教程", 6495407})
    fmt.Println(Books{title: "Go 语言", author: "www.runoob.com", subject: "Go 语言教程", book_id: 6495407})
    fmt.Println(Books{title: "Go 语言", author: "www.runoob.com"})
}
```

---

## 访问结构体成员

```go
package main

import "fmt"

type Books struct {
   title   string
   author  string
   subject string
   book_id int
}

func main() {
   var Book1 Books
   var Book2 Books

   Book1.title = "Go 语言"
   Book1.author = "www.runoob.com"
   Book1.subject = "Go 语言教程"
   Book1.book_id = 6495407

   Book2.title = "Python 教程"
   Book2.author = "www.runoob.com"
   Book2.subject = "Python 语言教程"
   Book2.book_id = 6495700

   fmt.Printf("Book 1 title : %s\n", Book1.title)
   fmt.Printf("Book 2 title : %s\n", Book2.title)
}
```

---

## 结构体作为函数参数

```go
func printBook(book Books) {
   fmt.Printf("Book title : %s\n", book.title)
   fmt.Printf("Book author : %s\n", book.author)
   fmt.Printf("Book subject : %s\n", book.subject)
   fmt.Printf("Book book_id : %d\n", book.book_id)
}
```

调用：

```go
printBook(Book1)
printBook(Book2)
```

---

## 结构体指针

```go
package main

import "fmt"

type Books struct {
   title   string
   author  string
   subject string
   book_id int
}

func printBook(book *Books) {
   fmt.Printf("Book title : %s\n", book.title)
   fmt.Printf("Book author : %s\n", book.author)
   fmt.Printf("Book subject : %s\n", book.subject)
   fmt.Printf("Book book_id : %d\n", book.book_id)
}

func main() {
   var Book1 = Books{"Go 语言", "www.runoob.com", "Go 语言教程", 6495407}
   var Book2 = Books{"Python 教程", "www.runoob.com", "Python 语言教程", 6495700}

   printBook(&Book1)
   printBook(&Book2)
}
```

---

### 17. Go 语言 `make`, `range`

#### `make` 关键字
`make` 关键字用于创建 **切片（slice）、映射（map）和通道（channel）**，它可以动态分配空间，避免手动初始化，提高代码效率。

##### 语法：
```go
make(T, length, capacity)
```
- `T`：要创建的类型（slice、map、channel）。
- `length`：指定长度（仅适用于 slice）。
- `capacity`：可选参数，仅适用于 slice，表示容量大小。

##### 示例：
```go
package main
import "fmt"

func main() {
    s := make([]int, 3, 5) // 创建切片，长度3，容量5
    fmt.Println(s, len(s), cap(s)) // 输出: [0 0 0] 3 5

    m := make(map[string]int) // 创建 map
    m["one"] = 1
    fmt.Println(m) // 输出: map[one:1]

    ch := make(chan int, 2) // 创建缓冲通道
    ch <- 10
    ch <- 20
    fmt.Println(<-ch, <-ch) // 输出: 10 20
}
```

---

#### `range` 关键字
`range` 关键字用于遍历数组（array）、切片（slice）、映射（map）、通道（channel）或字符串。

##### `range` 遍历数组和切片：
```go
package main
import "fmt"

func main() {
    nums := []int{1, 2, 3, 4}
    for index, value := range nums {
        fmt.Printf("index: %d, value: %d\n", index, value)
    }
}
```
输出：
```
index: 0, value: 1
index: 1, value: 2
index: 2, value: 3
index: 3, value: 4
```

##### `range` 遍历 Map：
```go
package main
import "fmt"

func main() {
    m := map[string]int{"a": 1, "b": 2, "c": 3}
    for key, value := range m {
        fmt.Printf("key: %s, value: %d\n", key, value)
    }
}
```

##### `range` 遍历字符串：
```go
package main
import "fmt"

func main() {
    for index, char := range "Go语言" {
        fmt.Printf("index: %d, char: %c\n", index, char)
    }
}
```

##### `range` 遍历通道：
```go
package main
import "fmt"

func main() {
    ch := make(chan int, 3)
    ch <- 1
    ch <- 2
    ch <- 3
    close(ch)

    for value := range ch {
        fmt.Println(value)
    }
}
```
输出：
```
1
2
3
```

---

### 总结：
✅ `make` 用于创建 slice、map 和 channel。
✅ `range` 用于遍历数组、切片、map、channel 和字符串。
✅ `range` 遍历 map 时顺序不固定。
✅ 遍历时可使用 `_` 忽略索引或值。


  

- Multiple Return Values （多返回值）
- Functions （函数）
  - `main` Function & `init` Function （main函数与init函数）
- `defer` Statement （defer 语句）
- Pointers （指针）
- Slice (`slice`) （切片）
- Map (`map`) （映射/哈希表）
- Interfaces (`interface`) （接口）
  - Empty Interface (`interface{}`) as a Universal Type （万能类型）
  - Type Assertion (`type assertion`) （类型断言）
- Struct (`struct`) （结构体）
  - Struct Tags (`struct tags`) （结构体标签）
- Reflection (`reflect`) （反射）
- Object-Oriented Features in Golang （Golang中的面向对象特性）
  - Encapsulation （封装）
  - Inheritance （继承）
  - Polymorphism （多态）

# Advanced Golang Concepts （Golang高阶）
- Goroutines (`goroutine`) - Lightweight Concurrency in Golang （Golang中的轻量级并发）
- Channels (`channel`) - Communication Between Goroutines （Goroutine 之间的通信）

# Go Modules & Package Management （Go modules 模块管理）

# Classic Golang Cases & Examples （Golang 经典案例）
