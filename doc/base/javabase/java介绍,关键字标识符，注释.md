#### 常见的计算机命令

 Dos窗口：`windows键+r`，在输入 `cmd`。 转到E盘：输入` E:`

`cd - 打开目录`  ---    `..` 表示上一层目录  ` .` 表示当前目录    `/`表示的是根目录 。例如：cd a；

`rmdir/rd - 删除目录`，当该目录下有子文件或者子目录的时候，无法删除

`mkdir/md - 创建目录`  例如：md a

`dir - 显示指定目录下`的所有子文件和子目录的

`tree` - 显示指定目录下的树状结构

#### Java介绍

   1995年由SUN公司推出的一门高级编程语言，面向互联网的编程语言，是WEB应用程序首选的语言，简单易学，安全可靠，`跨平台`。

#### 为什么Java语言能够跨平台？

 `Java虚拟机` - Java Virtual Machine - `JVM`，针对不同的操作系统，开发了不同的Java虚拟机，一段Java程序并不是直接运行在计算机上而是运行在Java虚拟机上，Java虚拟机将Java程序翻译成当前系统能够识别的命令。Java语言是跨平台的，但是Java虚拟机不是跨平台的。

   所有的JAVA程序是运行在JAVA虚拟机上的，JAVA虚拟机屏蔽了不同操作系统之间的差异性，使得相同的JAVA程序够在不同的操作系统上运行，从而实现了JAV 语言的跨平台。

注意：Java语言是跨平台的，但是Java虚拟机不是跨平台的

- JDK1.0 - JDK1.1 - 1.2（`Applet/swing---GUI动态网页`）
- JDK1.3 - JDK1.4 - 1.5(`枚举，反射JDK5.0,十个特性`)
- JDK6 - JDK7.0 - JDK8（`十个特性`）

Java之父：`James.GoslingJ`

#### Java的技术结构

`J2SE---标准版` - 为一些小应用程序与桌面程序提供了解决方案

`J2EE---企业版 `- 为企业中项目的开发提供了方案

`J2ME---移动版 `- 主要是嵌入一些小型电子设备中，实现移动端的开发

#### JDK，JRE，JVM

JVM - Java Virtual Mechine - `Java虚拟机`，是Java语言能够跨平台的前提

JRE - Java Runtime Environment - `Java运行时环境`。JRE中包含了核心类库和JVM。

JDK - Java Development Kit - `Java开发工具包`。包含了开发工具和JRE。

#### 下载JDK

`SUN地址`：https://www.oracle.com/   `ORACLE地址`：https://www.oracle.com

安装的时候不建议安装到C://program files目录下

- 注意：安装路径中不要出现空格和中文
- 将Java源文件翻译成及其能读懂的过程---编译
- 编译完成之后产生一个字节码文件（.class文件）

#### 入门程序

- Java程序所在的文件需要改成.java 
- Java程序运行的入口是主函数。没有主函数程序可以编译，但是不能运行
- class文件的文件名和类名对应
-  一个Java文件中可以写多个类，并且每个类对应一个class文件
- 一个Java文件中只能有一个公共类，但是可以有多个类

​    带包编译：`javac -d` 要编译到的位置 要编译的Java源文件

​                   `javac - d . Demo1.java`---其中有4处空格

​                   `java -cp class文件的存储位置 类的全路径名`（包名.类名）

#### 环境变量

目的：是为操作系统指定一些运行参数的量

​         `JAVA_HOME=Java的安装路径`

​         ` Path=%JAVA_HOME%\bin;`

   可以通过set 变量名=变量值; 的方式设置一个临时的环境变量，dos命令窗口关闭后，该临时变量随之消失

#### 关键字

定义：是只在Java中被赋予了特殊含义的单词。在Java中一共有`53个关键字`，其中51个在用，还有`2个`目前`没有使用`，称之为**`保留字 - const，goto`**。所有的`关键字都是小写`的

**用于定义数据类型的关键字**：class，interface，byte，short，int，long，float，double，char，boolean，void，enum。

**用于定义数据类型值的关键字**:  true，false，null。

**用于定义流程控制的关键字**：if， else， switch， case ，default， while，do， for，break， continue， return。

**用于定义访问权限修饰符的关键字**：private  protected  public

**用于定义类、函数、变量修饰符的关键字**：abstract  final  static  synchronized  

**用于定义类与类之间关系的关键字**： extends  implements

**用于定义建立实例、判断实例的关键字**：  new  this  super  instanceof

**用于异常处理的关键字**： try  catch  finally  throw  throws

**用于包的关键字 **： ackage  import              

**其他修饰符关键字**： native  strictfp  transient  volatile  assert

#### 标识符

定义：在程序中`自定义的名称`。

##### 定义规则

- 可以由字母、数字、_、$组成，不建议使用$符号
- 不能使用纯数字、数字不能作为开头
- 不能使用关键字
- Java是一门严格区分大小写的语言
- 为了提高程序的阅读性，尽量的见名知义
- 支持中文命名，但是不推荐

##### 驼峰命名法

**类名/接口名**：如果由多个单词组成，每个单词的首字母大写  HelloWorld。

**变量名/方法名**：如果由多个单词组成，第一个单词的首字母小写，其余单词的首字母大写  playGame

**包名**如果由多个单词组成，所有字母全部小写，中间用 . 隔开

**常量名**：如果由多个单词组成，所有字母全部大写，中间用_隔开

#### 注释

作用：在程序中用来解释或者说明程序的文字或者排错 

##### 格式

- //注释文字    `单行注释`
- /*注释文字*/   `多行注释`
-  /**注释文字*/  `文档注释`，往往用于注释类、方法或者常量

`javadoc -d .\\document Demo.java` - 这个命令只能用来提取公共类中文档注释的内容

   javadoc 要提取的java源文件--注意，一个类如果能够被提取，必须是公共类 （对这个类的说明书）（用工具可以提取不是公共类的）

**注释作用**：解释程序；便于阅读、维护；排错

 

 