[[dos简介]]
## 基本介绍
JVM帮助实现JAVA的跨平台性。
java程序通过javac编译形成的class文件，包含在JDK中,在JVM运行class文件。
JDK是java的开发工具包，包含JRE和JAVA的开发工具(java,javac,javadoc,javap)
1. java运行class文件
2. javac编译java文件
3. javadoc生成注释文档
4. javap反编译class文件
JRE是java的运行环境，包含JVM和java的核心类库


配置path环境变量的意义：当前执行的程序在当前的目录下如果不存在，windows系统会自动在path的环境变量目录中寻找，如果仍没有找到则弹出错误信息 

第一个程序
```
//这是java的快速入门，演示java的开发步骤
//1.public class Hello 表示Hello是一个类，是一个public公共的类
//2.Hello{}表示一个类的开始和结束
//3.public static void main(String[] args)表示一个主方法，程序的入口
//4.main(){}表示方法的开始和结束
//5.System.out.println("Hello world");表示输出到屏幕上，；表示语句的结束
public class Hello{
	//编写一个main方法
	public static void main(String[] args){
		System.out.println("Hello world");
	}
}
//bash 
//javac Hello.java 这里java源文件必须使用GBK编码，因为使用了中文
//java Hello 不加.java后缀的原因，找到Hello的主类运行，运行的是Hello的类，将class字节码文件放入JVM虚拟机中运行
```

## 注意细节
1. JAVA源文件是以.java为拓展名，源文件基本组成部分是类，如Hello类。
 1. java应用程序执行的入口是main()方法，拥有固定的书写格式：public static void main(String[] args){...}
 2. JAVA严格区分大小写
 3. JAVA语句必须以;结尾
 4. 大括号成对出现
 5. 一个源文件只有一个public类，其他类数量不限
 6. 编译后每一个类对应一个class文件
 7. java文件名必须与public类的名字一致
 8. 一个源文件只能有一个public类，其他类的数量不限制，也可以将main方法直接写到非public类中，运行非public类，这样入口方法就是非public的main方法
## 断点调试
1. 断点调试是指在程序的某一行设置一个断点，调试的时候程序运行到这一行代码就会停住，然后可以一步一步地往下运行，调试的过程中可以看各个变量的值，出错的话可以找到对应出错的代码行并且显示错误，并且进行分析找到这个bug
2. 断点调试是必备技能

| 快捷键操作   | 快捷键      |
| ------- | -------- |
| 跳入      | F7       |
| 跳过，逐行执行 | F8       |
| 执行下一个断点 | F9       |
| 跳出方法    | shift+F8 |
