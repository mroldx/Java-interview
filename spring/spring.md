#1. ApplicationContext 的初始化过程？初始化过程中发现循环依赖 Spring 是如何处理的。

#2. Spring IOC AOP


所谓循环依赖指的是：BeanA对象的创建依赖于BeanB，BeanB对象的创建也依赖于BeanA，这就造成了死循环，如果不做处理的话势必会造成栈溢出。
Spring通过提前曝光机制，利用三级缓存解决循环依赖问题。