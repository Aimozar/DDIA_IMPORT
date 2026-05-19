# 示例：事务隔离学习 Demo

## 场景

两个用户同时扣减同一个商品库存。

初始库存：

```text
stock = 1
```

两个请求同时执行：

```sql
SELECT stock FROM inventory WHERE product_id = 100;
UPDATE inventory SET stock = stock - 1 WHERE product_id = 100;
```

## 可能问题

如果没有正确并发控制，两个请求都认为库存足够，最终可能导致超卖。

## 解决方案 1：数据库行锁

```sql
SELECT stock FROM inventory WHERE product_id = 100 FOR UPDATE;
```

适合：强一致要求、并发量可控。

缺点：锁竞争、性能下降。

## 解决方案 2：乐观锁

```sql
UPDATE inventory
SET stock = stock - 1
WHERE product_id = 100
  AND stock > 0;
```

判断影响行数：

- 1：扣减成功
- 0：库存不足或并发失败

适合：高并发、简单库存扣减。

## 解决方案 3：Redis 预扣 + MQ 异步确认

适合：秒杀、高并发抢购。

风险：Redis 和数据库最终一致，需要补偿和对账。

## DDIA 对应知识

- ch7：事务、隔离、丢失更新
- ch8：故障、重试、幂等
- ch11：消息队列、事件处理
