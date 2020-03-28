## 加入nest.js
> Spring-它通过灵活使用控制反转、依赖注入和面向切面编程等设计理念，极大的规范了大型应用的架构，降低了模块之间的耦合度，从而提升了应用的开发效率。nest.js借鉴了其思想


### 官网讲的三个特点
可扩展
多才多艺
先进 --  把设计模式和成熟的解决方案带入node

### 几个核心概念
依赖注入、控制反转、
依赖注入--> 代码解耦
面向切面编程。可以集中进行异常处理、数据验证、权限验证、逻辑扩展。

![undefined](http://ww1.sinaimg.cn/large/006x4mSygy1gd9yeg2vatj30m80d4dhp.jpg)
![undefined](http://ww1.sinaimg.cn/large/006x4mSygy1gd9yexin8oj30m804bmxq.jpg)

### SOLID原则


### 核心模块
Controller
Providers
    提供程序是Nest的基本概念。
    许多基本的Nest类都可以被视为提供程序-服务，存储库，工厂，帮助程序等。
    提供程序的主要思想是它可以注入依赖项。
    这意味着对象可以彼此创建各种关系，并且“连接”对象实例的功能在很大程度上可以委托给Nest运行时系统。
    提供者只是一个用@Injectable（）装饰器注释的类
Modules
Middleware
Exception filters
Pipes
Guards
Intercetpors
Custom decorators


### 大杂烩
1. 可以利用express访问原生request和res对象
2. 控制器负责处理传入的请求并将响应返回给客户端。