# complier 一个简单的语言

**变量类型**

```c
// 初始化 
var a : int = 1

int     1, 2, 3
float   2.5, 0.6
str     "字符串"
bool ture, false
list[1, 2, 3]
dict    {
"1":"a", "2":"b", "3":"c"
}
```

---
**关键字**

|   关键字    |  说明  |
|:--------:|:----:|
|   var    | 变量定义 |
|   int    |      |
|  float   |      |
|   str    | 字符串  |
|   bool   | 布尔类型 |
|   list   |  数组  |
|   dict   |  字典  |
|   ture   |      |
|  false   |      |
|    if    |      |
|   else   |      |
|   elif   | 再次判断 |
|   for    |      |
| continue |      |
|  break   |      |
|   fun    | 方法定义 |
|  return  |      |
|   pack   | 数据集合 |
|  import  |  引入  |

---
**运算符**

|     运算符      |  描述  |
|:------------:|:----:|
|      []      | 数组下标 |
|      ()      |      |
|      .       | 成员选择 |
|      -       | 算数负号 |
|      *       | 地址取值 |
|      !       | 逻辑非  |
|      ~       | 按位取反 |
|      /       |      |
|      *       |      |
|      %       |      |
|      +       |      |
|      -       |      |
|      <<      |      |
|     \>>      |      |
|      \>      |      |
|     \>=      |      |
|      <       |      |
|      <=      |      |
|      ==      |      |
|      !=      |      |
|      &       | 按位与  |
|      ^       | 按位异或 |
|    &#124;    | 按位或  |
|      &&      | 逻辑与  |
| &#124;&#124; | 逻辑或  |
|      =       |      |
|      /=      |      |
|      *=      |      |
|      +=      |      |
|      -=      |      |
|      ,       |      |

---
**条件语句**

```c
if (a < b) { 语句 }
if (a < b) { 语句 } else { 语句 }
if (a == b) { 语句 } elif(a == c) { 语句 } else { 语句 }

if (a < b) 单条语句
if (a < b) 单条语句 else 单条语句
if (a == b) 单条语句 elif(a == c) 单条语句 else 单条语句

// 三元表达式
var a, b = 1, 1
var result: str = a==b ? "a==b" ： "a!=b"
print(resutl) // a==b
```

---
**循环语句**

```c
for (变量: 可迭代量) 单条语句
for (变量: 可迭代量) { 语句 }

// 次数循环
for (i: 2..10) { 
    print(i) // 2, 3,..., 9, 10
}

// 数组循环
var lists = ["a", "b", "c"]
for (i: lists) { 
    print(i) // a, b, c
}

// 字典循环
var dicts = {"a":123, "b":456, "c":789}
for (key, value: dicts) { 
    print(key, ":",value) // a:123, b:456, c:789
}
```

---
**枚举**

```c
enum Fruit {
    Apple,
    Banana,
    Cherry
}
```

---
**函数（方法）**

```c
// 定义
fun do_something(in: int) : Fruit {
if (in == 1)
return Fruit.Apple
elif (in == 2)
return Fruit.Banana
else
return Fruit.Cherry
}

// 主函数 (程序入口)
fun main（） {
var result: Fruit = do_something(3)
print(result) // Cherry
}
```

---
**数据集合（数据与函数的集合而已）**

```c
// 定义：
pack Student {
var name: str
var age: int
var class: str
var score: float = 0

fun prints() {
print(name, age, class, score)
}
}

// 初始化：
var s1 = Student("张三", 18, "高三（3）班")

var s2 = Student("李四", 17)
s2.class = "高三（4）班"
s2.score = 115

// 使用:
s1.prints()     // 张三, 18, 高三（3）班, 0
s2.prints()     // 李四, 17, 高三（4）班, 115
```
 