# wishdata-cloud
智数通2.0是新一代完全自主研发的数据治理平台，现拥有数据建设平台、数据治理平台、数据服务平台、任务调度平台等四大基础数据治理平台，
实现了数据集成、元数据管理、数据标准管理、数据质量管理、数据服务管理、数据建模管理、数据血缘查看、数据资产管理、任务调度管理等功能模块，
打通了数据治理各个环节，快速满足政府、企业各类不同的数据治理场景。

系统架构：以Hadoop、Hive等组件为中心的架构体系。
数据架构：顶层设计，主题域划分，分层设计，ODS-DW-ADS
数据建模：维度建模，业务过程-确定粒度-维度-事实表
数据管理：元数据管理、数据标准、数据质量管理、数据资产管理
辅助系统：分布式调度、数据集成
数据服务：API开发、可视化系统（暂无）
该系统主要基于Hadoop + Hive构建企业级数据仓库，数仓层大致划分成为贴源层，公共层，应用层3层，细分为ODS数据引入层，DIM公共维度层，DWD明细数据层，DWS汇总数据层，ADS应用数据层。
Hive是建立在Hadoop上的数据仓库基础架构。它提供了一系列的工具，用来进行数据提取、转换、加载，这是一种可以存储、查询和分析存储在Hadoop中的大规模数据机制。可以把Hadoop下结构化数据文件映射为一张成Hive中的表，并提供类sql查询功能，除了不支持更新、索引和事务，sql的其它功能都支持。可以将sql语句转换为MapReduce任务进行运行，作为sql到MapReduce的映射器。

源码没有开源，如果公司有数据治理这方面需要的可以联系，毕竟开发起来并不容易，会收取点辛苦费用，希望大家可以理解。
QQ 312075478 请备注来源（wishdata-cloud）

后端技术栈
•	开发框架：Spring Boot 2.7.9
•	微服务框架：Spring Cloud Alibaba 2021.0.4.0
•	安全框架：Spring Security + Spring OAuth 2.0 
•	持久层框架：MyBatis Plus
•	数据库连接池：Hikaricp
•	服务注册与发现: Nacos
•	客户端负载均衡：Spring Cloud Starter Loadbalancer
•	熔断组件：Resilience4j
•	网关组件：Spring Cloud Gateway
•	缓存：Redis
•	分布式调度：Zookeeper + Netty
•	日志管理：Logback
•	运行容器：Undertow
前端技术栈
•	JS框架：Vue 3
•	CSS框架：Less
•	组件库：Naive UI
•	打包构建工具：VIte

模块说明
wishdata-cloud
├── wishdata-gateway -- 网关[8801]
├── wishdata-auth -- 授权服务提供[8802]
├── wishdata-common -- 系统公共模块
├── wishdata-modules -- 业务模块
├    ├── wishdata-dap – 数据建设平台[8804]
├    ├── wishdata-dgp – 数据治理平台[8805]
├    ├── wishdata-dsp – 数据服务平台[8806]
├    ├── wishdata-smp – 系统管理平台[8803]
├    ├── wishdata-tsp –任务调度平台[8807]
├    ├── wishdata-tsp-master –调度节点 [8871]
├    ├── wishdata-tsp-worker –执行节点[8872]
├── wishdata-plugins -- 相关插件
├    ├── wishdata-plugin-driver – 数据源驱动插件
├    ├── wishdata-plugin-driver-api – 数据源驱动插件接口
├    ├── wishdata-plugin-driver-starter – 数据源驱动插件集成springboot

[智数通-数据建设平台.docx](https://github.com/yuwei1203/wishdata-cloud/files/10986641/-.docx)
[智数通-数据治理平台.docx](https://github.com/yuwei1203/wishdata-cloud/files/10986661/-.docx)
[智数通-数据服务平台.docx](https://github.com/yuwei1203/wishdata-cloud/files/10986662/-.docx)
[智数通-任务调度平台.docx](https://github.com/yuwei1203/wishdata-cloud/files/10986663/-.docx)
