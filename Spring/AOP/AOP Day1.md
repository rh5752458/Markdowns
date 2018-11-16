# AOP 面向切面编程

- Aspect-Oriented Programming
- 把每个类中重复的事务型代码抽出

## 代理模式
> 代理提供了对目标对象额外的访问方式,即通过代理对象来访问目标对象.

>  这样可以在不修改原目标对象的前提下,提供额外的功能操作,扩展目标对象的功能.

> 简言之,代理模式就是设置了一个中间代理来控制访问原目标对象,以达到增强原对象的功能和简化访问方式


#### I.静态代理:
> 这种代理方式需要代理对象和目标对象实现一样的接口,

> 把java源文件编译成class文件过程中改变执行结果(扩展功能)

- 优点:可以在不修改目标对象的前提下扩展目标对象的功能
- 缺点:
    + 冗余.由于代理对象要实现与目标对象一致的接口,会产生过多的代理类
    + 不易维护.一旦接口修改方法,代理对象和目标对象都得进行修改
- 静态代理实例: 装饰者模式
- 静态代理框架: AspectJ


    方法1: 实现接口
    方法2: 继承

#### II.动态代理:
> 动态代理利用了JDK API,动态的在内存中构建代理对象,从而实现对目标对象的代理功能.动态代理又被称为JDK代理或接口代理。

>把字节码运行到JVM虚拟机的过程中改变执行结果
- 特点: 动态代理对象不需要实现接口,但要求目标对象必须实现接口,否则不能用动态代理
- 动态代理实例
    + 使用的JDK反射框架下的代理类,只能针对有接口的类进行扩展功能
    + 使用第三方的CGLib框架,只能针对没有有接口但是可继承的类进行扩展功能



#### III.静态代理与动态代理的区别
1. 静态代理是在编译时就已经实现,编译完成后代理类是一个实际的class文件
2. 动态代理是在运行时动态生成的,即编译完成后没有实际的class文件,而是在运行时动态生成类字节码,并加载到JVM中.



#### 动态代理 第三方 CGLib 框架
- 配置

```xml
<dependency>
    <groupId>cglib</groupId>
    <artifactId>cglib</artifactId>
    <version>3.1</version>
</dependency>
```


### Spring 框架的 AOP
/*
面向切面编程 (AOP) 实际上在做什么?
- 规定在代码的某个位置 (何处) 的什么时候 (何时) 做什么事情 (什么)
- 比如: 在登录的方法执行之前打印日志
-    何处: 登录的方法
-    何时: 执行之前
-    什么: 打印日志

1. 接入点 JoinPoint
    可以为其插入增强功能代码的位置 (即方法) 叫做接入点.
    在 Spring 中 JoinPoint 是一个类, 代表被增强了的方法.

2. 切点 PointCut
    实际上是一个表达式, 表示哪些方法需要被增强. (何处)

3. 通知 advice
    通知的作用是对切点所描述的方法进行增强, 在何时如何增强. (何时)(什么)
    五种通知:
        <1> 前置通知: 方法执行之前
        <2> 后置通知: 方法执行之后 (无论出不出异常)
        <3> 返回通知: 代表方法正常执行
        <4> 异常通知: 出现异常
        <5> 环绕通知

4. 切面 aspect
    {切点} 和 {通知} 组成 {切面}

5. 织入 weave
    表示的是把切面与目标整合起来的过程
*/

- 创建切面类

```java
public void logBefore() {
    System.out.println("方法执行之前");
}

public void logAfter() {
    System.out.println("方法执行之后");
}

public void logAfterThrow() {
    System.out.println("方法抛异常了");
}

public void logAfterReturn() {
    System.out.println("方法正常执行了");
}
```

- 配置 SpringAOP
    - 创建 xml 配置文件

```xml

```