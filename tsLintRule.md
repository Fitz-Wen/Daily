# TSLint 规则
来源于[链接](https://palantir.github.io/tslint/rules/)

## no-any

**说明**：不允许使用any类型
### 设置
 ```
    "no-any": true
 ```
 ```
    "no-any": [true, {"ignore-rest-args": true}]
 ```
 ---
 ## no-empty-interface

**说明**：禁止空接口
### 设置
 ```
    "no-empty-interface": true
 ```
 ---
 ## no-for-in

**说明**：禁止使用for-in语句
### 设置
 ```
    "no-for-in": true
 ```
  ---
 ## forin

**说明**：使用for···in语句必须用if进行判断
```
for (let key in someObject) {
    if (someObject.hasOwnProperty(key)) {
        // code here
    }
}
```
### 设置
 ```
   "forin": true
 ```
---
## function-constructor

**说明**：防止使用Function申明函数
```
let doesNothing = new Function();
```
### 设置
 ```
   "function-constructor": true
 ```
 
---

## no-arg

**说明**：禁止使用arguments.callee

### 设置

 ```
   "no-arg": true
 ```
 
---

## no-console

**说明**：禁止使用控制台方法

### 设置

 ```
  "no-console": [true, "log", "error"]
 ```
 如没有设置方法名称，则禁止所有控制台方法。
 
---

## no-debugger

**说明**：禁止使用debugger

### 设置

 ```
  "no-debugger": true
 ```
 ---

##  no-duplicate-variable

**说明**：同一作用块不允许使用相同声明名

### 设置

 ```
  "no-duplicate-variable": true
 ```
 ---

##  no-dynamic-delete

**说明**：禁止使用delete

### 设置

 ```
  "no-dynamic-delete": true
 ```
---
## no-empty

**说明**：禁止块作用域中为空

### 设置

 ```
  "no-empty": true
 ```
 ```
    "no-empty": [true, "allow-empty-catch"]
    "no-empty": [true, "allow-empty-functions"]
    "no-empty": [true, "allow-empty-catch", "allow-empty-functions"]
 ```
 ```allow-empty-catch```, ```allow-empty-functions```是允许catch和function中为空
 
---

##  no-eval

**说明**：禁止使用eval

### 设置

 ```
  "no-eval": true
 ```
---

## no-shadowed-variable

**说明**：不允许跟踪变量声明
如
```
const a = 'no shadow';
function print() {
    const a = 'shadow'; // TSLint will complain here.
    console.log(a);
}
print(); // logs 'shadow'.
```

### 设置

 ```
  "no-shadowed-variable": true
 ```
---

## switch-default

**说明**：switch语句必须包含default语句

### 设置

 ```
  "switch-default": true
 ```
---
## triple-equals

**说明**：使用```===```代替```==```,```!==```代替```!=```

### 设置

 ```
  "triple-equals": true
 ```
---

## unnecessary-constructor

**说明**：防止空的构造函数

### 设置

 ```
  "unnecessary-constructor": true
 ```
---

## use-isnan

**说明**：使用```isNaN()```判断是否为NaN

### 设置

 ```
  "use-isnan": true
 ```
---

## cyclomatic-complexity

**说明**：圈复杂度

### 设置
最小值为2，默认为0
 ```
  "cyclomatic-complexity": true
 ```
 ```
  "cyclomatic-complexity": [true, 10]
 ```
---

##  max-classes-per-file

**说明**：一个文件中类的最大个数

### 设置

 ```
 "max-classes-per-file": [true, 1]
 ```
---

##  max-classes-per-file

**说明**：一个文件中类的最大个数

### 设置

 ```
 "max-classes-per-file": [true, 1]
 ```
---

##  max-file-line-count

**说明**：一个文件中代码行数的最大值

### 设置

 ```
 "max-file-line-count": [true, 300]
 ```
 ---

## prefer-const

**说明**：尽可能使用```const```代替```var```或者```let```

### 设置

 ```
"prefer-const": true
 ```
 
---
## binary-expression-operand-order

**说明**：表达式中变量应尽可能靠左，文字靠右。如```x + 1```,而不是```1 + x```

### 设置

 ```
"binary-expression-operand-order": true
 ```

---
## class-name

**说明** ```class```和```interface```的命名应遵循首字母大写

### 设置

 ```
"class-name": true
 ```

---
##  encoding

**说明** 使用```UTF-8```编码

### 设置

 ```
"encoding": true
 ```

---
##  file-name-casing

**说明** 统一文件命名规范

### 设置

 ```
 fileName.ts
"file-name-casing": [true, "camel-case"]
 ```
```
FileName.ts
"file-name-casing": [true, "pascal-case"]
```
```
file-name.ts
"file-name-casing": [true, "kebab-case"]
```
```
file_name.ts
"file-name-casing": [true, "snake-case"]
```
---
##  no-boolean-literal-compare

**说明** 不允许与布尔值进行比较，如```x === true```

### 设置
```
"no-boolean-literal-compare": true
```
---
## one-variable-per-declaration

**说明** 不允许多个变量在同一行声明
如
```
const foo = 1;
const bar = '2'; // good
```
```
const foo = 1, bar = '2'; // bad
```
### 设置
```
"one-variable-per-declaration": true
```

---
## indent

**说明** 缩进

### 设置
```
"indent": [true, "tabs", 2]
```
```
"indent": [true, "spaces", 4]
```
---
## max-line-length

**说明** 每行代码最大长度

### 设置
```
"max-line-length": [true, 80]
```

---
## max-line-length

**说明** 每行代码最大长度

### 设置
```
"max-line-length": [true, 80]
```
---
## no-trailing-whitespace

**说明** 行尾不允许出现空格

### 设置
```
"no-trailing-whitespace": true
```

---
## number-literal-format

**说明** 使用```.```代替```0.```

### 设置
```
"number-literal-format": true
```
---
## quotemark

**说明** 引号设置

### 设置
```
"quotemark": [true, "single"]
```

---
## semicolon

**说明** 分号设置

### 设置
```
"semicolon": [true, "always"]
```
---
## curly

**说明** ```if/for/do/while```后必须通过 ```{}``` 包裹代码块

### 设置 
```
"curly": true
```
---
## eofline

**说明** 文件必须用新换的行结束

### 设置 
```
"eofline": true
```
---
## interface-over-type-literal

**说明** 声明```interface``` 接口，代替```type```关键字声明类型

### 设置 
```
"interface-over-type-literal": true,
```