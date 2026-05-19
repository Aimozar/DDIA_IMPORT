# Java 后端视角 DDIA 核心术语

## 可靠性 Reliability

系统在硬件故障、软件 bug、人为错误、网络异常等情况下仍然尽量正确工作。

Java 后端场景：服务降级、超时重试、熔断、数据备份、灰度发布。

## 可伸缩性 Scalability

系统面对数据量、请求量、复杂度增长时，仍能通过合理增加资源维持性能。

Java 后端场景：水平扩容、分库分表、缓存、异步化、读写分离。

## 可维护性 Maintainability

系统长期演进时，开发者仍能理解、修改、排障和扩展。

Java 后端场景：模块化、清晰 API、可观测性、测试、文档。

## 索引 Index

用于加速查询的数据结构，本质是在写入成本和读取性能之间做取舍。

Java 后端场景：MySQL 联合索引、覆盖索引、慢 SQL 优化。

## 复制 Replication

把同一份数据复制到多个节点，用于提高可用性、读性能和容灾能力。

Java 后端场景：MySQL 主从、Redis 主从、Elasticsearch 副本。

## 分区 Partitioning

把大数据集拆分到多个节点，解决单机容量和性能瓶颈。

Java 后端场景：分库分表、分片、水平拆分。

## 事务 Transaction

把多个读写操作组合成一个逻辑单元，要么全部成功，要么失败回滚。

Java 后端场景：Spring @Transactional、订单创建、库存扣减、账户转账。

## 隔离性 Isolation

多个事务并发执行时，彼此可见程度的控制。

Java 后端场景：脏读、不可重复读、幻读、丢失更新、写偏斜。

## 线性一致性 Linearizability

系统表现得像只有一份最新数据副本，每次读都能看到最近完成的写。

Java 后端场景：强一致配置中心、分布式锁、选主。

## 共识 Consensus

多个节点在可能发生故障的情况下，就某个值或决策达成一致。

Java 后端场景：ZooKeeper、etcd、Raft、leader election。

## 幂等 Idempotency

同一个操作执行多次和执行一次效果相同。

Java 后端场景：支付回调、MQ 重复消费、重试下单、接口防重。

## 派生数据 Derived Data

从原始数据通过计算、索引、缓存、同步得到的数据。

Java 后端场景：Redis 缓存、Elasticsearch 搜索索引、统计表、物化视图。
