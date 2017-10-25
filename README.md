# gcoordinator
从数据库中获取新增订单，触发delivery2.0开通资源

业务逻辑设计
1. 使用linux conrtab作为定时器
2. 从mysql数据库中查看是否有新订单。
3. 如果有新订单，把订单关联的note中text字段更新为Paid
4. 调用delivery2.0的开通（CVM）接口
