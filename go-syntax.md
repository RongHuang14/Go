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
