如果并发量比较大 数据库来不及修改 状态未修改 导致后面逻辑没执行

修改方案:改用@TransactionalEventListener 确保事务提交后执行 TransactionPhase.AFTER_COMMIT