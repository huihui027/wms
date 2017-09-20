# wms
开源Java仓库管理系统

此WMS目标, 轻松支持日均10万单量. 水平扩展能力一般. 

架构很简单,没有最新最热的技术,框架.

我会另外建一个基于分布式服务框架的项目架构,需要将WMS微服务化的话,就要自己动手转化了.

以下是技术选型,
项目管理:maven

代码管理:git

缓存：Redis    (基础数据,会话共享) 会话是自己做的session, 使用cookie+ 缓存替代 HttpSession

消息中间件：ActiveMQ

负载均衡：Nginx

数据库连接池：Alibaba Druid 1.0

核心框架：Spring framework

视图框架：Spring MVC 4.0

任务调度：quartz (实现集群,持久化,界面化动态管理)

持久层框架：MyBatis 3.2 (结合代码生成,分页插件)
分页插件是一个真正的分页插件, 跟网上很多共享的把原sql包一层 select(*) from ( 原查询sql ) 这种垃圾插件不一样.

日志管理：SLF4J 1.7、Log4j

API网关:Kong 

//编码约定
//缓存方案
//事务控制
//异常处理
//部署方案
待补全....
