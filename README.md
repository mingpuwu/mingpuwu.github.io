## Welcome to GitHub Pages

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

# UML
### 依赖
- 使用关系(局部变量、方法的参数、对静态方法的调用)
![依赖](https://upload-images.jianshu.io/upload_images/16628722-89a9f914670089f8.png)
### 关联
- 整体和部分的关系，关联涉及的两个类在同一个层次上(成员变量)
![关联](https://upload-images.jianshu.io/upload_images/16628722-92f84cb2b50052ab.png)
### 聚合
- 整体和部分的关系，可以分开，弱拥有关系(成员变量)
![聚合](https://upload-images.jianshu.io/upload_images/16628722-31f866d3f7dea3dc.png)
### 组合
- 整体和部分的关系，不可分开，部分的生命周期和整体的生命周期同生死(new出来的)
![组合](https://upload-images.jianshu.io/upload_images/16628722-694e896c65cd3351.png)
### 继承
![继承](https://upload-images.jianshu.io/upload_images/16628722-6e1f08d83deb27b7.png)
### 实现
![实现](https://upload-images.jianshu.io/upload_images/16628722-e136f4d97fea788e.png)
### Support or Contact


