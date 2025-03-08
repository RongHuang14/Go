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
	•	fmt 是 Go 标准库（package），用于格式化 I/O（输入输出），类似于 Python 里的 print()，C 语言的 printf()。
	•	Println 是 fmt 包中的一个函数，用于输出内容并自动换行。
 <img width="842" alt="image" src="https://github.com/user-attachments/assets/e1bb8148-f8cc-4dac-a88e-1b06fb8884c7" />


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

#### **变量声明**
```go
var a string = "Runoob"
fmt.Println(a)

var b, c int = 1, 2
fmt.Println(b, c)
```

#### **零值概念**
```go
var a string  // 默认零值 ""
var b int     // 默认零值 0
var c bool    // 默认零值 false
fmt.Println(a, b, c)
```

#### **短变量声明（仅限函数内部）**
```go
d := true
fmt.Println(d)
```

#### **多变量声明**
```go
var (
    x, y int
    a int
    b bool
)
var c, d = 1, 2
var e, f = 123, "hello"

g, h := 123, "hello"  // 只能在函数体内使用
fmt.Println(x, y, a, b, c, d, e, f, g, h)
```

#### **并行赋值**
```go
a, b := 5, 7
fmt.Println(a, b)  // 5, 7

// 变量交换
a, b = b, a
fmt.Println(a, b)  // 7, 5
```

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
