# study-summary
学习总结，包括知识技能等

## 设计模式学习
1. adapter 适配器模式
2. bridge 桥模式
3. builder 建造者模式
4. chain.responsibility 责任链模式
5. composite  聚合
6. decorator  装饰者模式
7. delegate 委派模式
8. facade 
9. factory 简单工厂.抽象工厂.工厂方法.工厂单例；
10. observer 观察者模式
11.proxy 代理模式  静态代理.cglib 代理.
12.singleton 单例模式
13. strategy 策略模式
14. template.method  模板方法


## mysql事务

### 事务的特性

1. A atomicity 原子性；
2. C consistency 一致性；
3. I isolation 隔离性；
4. D Durability    持久性；

### 事务的隔离级别

1. Read uncommited 读未提交；
2. Read Commited  读已提交；
3. Repeated Read   可重复读；
4. Serializable   序列化；

这四种隔离级别可能有的问题

^ 隔离级别  ^ 脏读 ^ 不可重复读 ^ 幻读 ^ 
| Read Uncommited | 可能 | 可能 | 可能 | 
| Read Commited | 不可能 | 可能 | 可能 | 
| Repeated Read | 不可能 | 不可能 | 可能 | 
| Serializable | 不可能 | 不可能 | 不可能 | 

幻读无法通过行锁来避免，幻读重点是insert，所以无法通过行锁还避免，因为在insert前，这条记录就不存在。

### innoDB 如何保证的事务的特性

1. A atomicity 原子性；
3. I isolation 隔离性；

InnoDB通过MVCC(多版本并发控制)来保证隔离性；

MVCC(多版本并发控制) 主要解决了读写的冲突，在保证读与写隔离性的同时，保证数据库的高并发性；

引入了MVCC后，数据库中的读分为2种，分别是当前读和快照读；

当前读是 insert、update、delete 、select for update 、 select  with shared lock(好像是这种select)

4. D Durability    持久性；
5. C consistency 一致性；






















