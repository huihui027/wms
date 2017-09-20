# wms
开源Java仓库管理系统

此WMS目标, 轻松支持日均10万单量. 水平扩展能力一般. 

架构很简单,没有最新最热的技术,框架.

我会另外建一个基于分布式服务框架的项目架构,需要将WMS微服务化的话,就要自己动手转化了.

以下是技术选型

项目管理:maven

代码管理:git

缓存：Redis

消息中间件：ActiveMQ

负载均衡：Nginx

数据库连接池：Alibaba Druid 1.0

核心框架：Spring framework

视图框架：Spring MVC 4.0

任务调度：quartz

持久层框架：MyBatis 3.2 

日志管理：SLF4J 1.7、Log4j

API网关:Kong 

其中:
quartz:(实现集群,持久化,界面化动态管理)

redis 用于缓存基础数据,会话; 会话是自己做的session, 使用cookie+ 缓存替代 HttpSession

mybatis 结合代码生成工具,分页插件

代码生成工具可以生成entity,mapper,service,controller, 还有仿hibernate的criteria, 单表操作完全不用写sql.

分页插件是一个真正的分页插件, 跟网上很多共享的把原sql包一层 select count(*) from ( 原查询sql ) 这种没用的插件不一样.

框架还有其他地方的处理,如使用过滤器 全局trim参数, aop 处理异常,日志,统一后端返回消息封装,前端框架表格,弹窗,form提交等都是经过封装改造. 
总的来说,除了没使用微服务架构,其他方面架构能统一处理的地方,基本处理了.

//编码约定
//缓存方案
//事务控制
//异常处理
//部署方案
待补全....
