## Welcome to GitHub Pages

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

# code-rules

### 头文件
- 头文件要自给自足
- 实体中尽量避免使用前置声名
- 内联函数，小于10行，代码功能简单.其次，内连函数必须放在.h中
- include顺序、依赖哪些就需要包含哪些

### 作用域
- 头文件中不要使用using声名(using namespace xxx;)
- 励在 .cc 文件内使用匿名命名空间或 static 声明，但是不要在.h中用
- 禁止使用using指示(using namespace std)，鼓励使用using声名(using std::string)
- 禁止在.h中使用命名空间别名

### 类
- 构造函数禁止调用虚函数，不要在构造中进行可能失败的初始化
- 对于单参构造函数加 explicit关键字
- 使用组合常常比使用继承更合理，分清is-a、has-a，禁止滥用继承

### 函数
- 入参在前，输出参数在后
- 短于50行
- 如果是引用的话必须为const

### 命名约定
- 类型命名每个首字母必须大小写，不包含下划线
- 变量命名必须小写，单词间用下划线连接，类成员变量需要以下划线结尾
- 结构体中的变量不必遵守类变量的命名规则
- 常量命名以k开头，大小写混合写
- 函数命名用驼峰式，但是对于protected和privated函数首字母要小写
- 命名空间全小写


### Support or Contact


