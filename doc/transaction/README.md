# 事务控制

## 场景-变更审批流程状态的同时记录一次操作详情  
变更审批流程状态的同时记录一次操作详情，变更审批流程的状态会在数据库中更新审批流程表的状态字段，同时通过在表b插入一条新的记录来记录这次操作详情。

### sql操作  
将业务简化为两个步骤：  
* 更新表a的字段  
* 在表b中记录本次操作详情  

### Node示例
