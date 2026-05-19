# DDIA 章节学习地图：Java 后端视角

## ch1 可靠性、可伸缩性和可维护性

后端价值：建立系统设计评价框架，理解可靠性、扩展性、可维护性的取舍。

Java 对应：服务降级、熔断限流、灰度发布、日志监控、可观测性。

## ch2 数据模型与查询语言

后端价值：理解关系模型、文档模型、图模型的差异，选择 MySQL、MongoDB、图数据库时更有依据。

Java 对应：MyBatis / JPA 实体建模、JSON 字段、多对多关系、复杂查询。

## ch3 存储与检索

后端价值：理解数据库为什么需要索引，理解写入、读取、压缩、合并的成本。

Java 对应：MySQL 索引优化、慢 SQL 排查、B-Tree、LSM Tree、ClickHouse、Elasticsearch。

## ch4 编码与演化

后端价值：理解接口升级、数据格式演化和兼容性，避免微服务接口升级事故。

Java 对应：JSON、Protobuf、Avro、RPC、REST API 版本兼容。

## ch5 复制

后端价值：理解高可用、读扩展、主从延迟和数据丢失风险。

Java 对应：MySQL 主从复制、Redis 主从复制、读写分离、用户写完马上读不到数据。

## ch6 分区

后端价值：理解大数据量如何横向扩展，以及分库分表的复杂性。

Java 对应：ShardingSphere、分库分表、热点 key、全局唯一 ID、跨分片查询。

## ch7 事务

后端价值：理解 ACID 与事务隔离，处理并发更新、库存扣减、账户转账。

Java 对应：Spring `@Transactional`、MySQL MVCC、隔离级别、丢失更新、写偏斜、分布式事务。

## ch8 分布式系统的麻烦

后端价值：理解网络不可靠、超时不可靠、时钟不可靠，正确设计重试、幂等和降级。

Java 对应：Dubbo / Spring Cloud、Feign 超时、重试风暴、幂等设计、雪崩保护。

## ch9 一致性与共识

后端价值：理解一致性模型、选主问题和分布式锁风险。

Java 对应：ZooKeeper、etcd、Redis 分布式锁、线性一致性、Raft、配置中心。

## ch10 批处理

后端价值：理解离线数据处理、大规模日志、报表、ETL。

Java 对应：Hadoop、Spark、离线任务、报表统计、数据仓库。

## ch11 流处理

后端价值：理解事件驱动架构、消息队列、CDC、实时计算。

Java 对应：Kafka、RocketMQ、Flink、Canal、Debezium、订单事件流。

## ch12 数据系统的未来

后端价值：建立整体架构观，理解派生数据、数据集成、端到端正确性。

Java 对应：CQRS、读写模型分离、缓存、索引、物化视图、数据一致性治理。
