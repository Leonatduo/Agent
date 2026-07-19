milvus是企业级生产级别数据库

milvus基本概念：
collection集合: 对应数据库中的表概念
schema: 对应数据库中的表字段关系
index: 类似于字典的目录， 加速检索
entity:具体存在milvus中的一条数据
partion: 存在milvus中的每条数据都根据语义被归在某一个分区中， 作用是加速检索
alias： 因为大规模向量数据迁移的时候如果从原collection迁移必须停机进行， 所以为了避免停机， 服务请求都是用collection的别名， 然后改了表结构什么的从原表中的最新数据搬到最新的collection中然后新collection的别名取为访问的， 这样就实现了无感
数据迁移。

