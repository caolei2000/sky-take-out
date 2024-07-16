# 外卖点餐平台  

一个基于 Spring Boot+MySQL+MyBatis+Redis 的外卖点餐平台。该项目分为客户端和商家端。商家端主要实现了员工管理、菜品管理和订单管理等功能。客户端基于微信小程序，提供了在线点餐、下单和催单等功能。

技术栈：Spring、Spring MVC、Spring Boot、MySQL、MyBatis、Redis、JWT  

核心功能： 
1. 登录校验：采用 JWT 令牌技术进行会话跟踪，通过拦截器统一拦截请求，解决 HTTP 请求的无状态问题，实现用户登录校验。
2. 用户身份管理：使用 ThreadLocal 方便且安全地管理应用中的用户身份，确保线程安全和数据隔离。
3. 公共字段自动填充：基于 AOP 实现公共字段（如创建时间、创建人）的自动填充，降低耦合度，简化后续代码开发。
4. OSS 存储与 Redis 缓存：使用阿里云 OSS 存储菜品和套餐图片，通过 Redis 对菜品信息进行缓存，减轻高并发环境下数据库的压力，提高系统性能。
5. 定时任务处理：利用 Spring Task 实现订单状态的定时处理功能，例如自动取消超时订单。
6. 长连接通信：通过 WebSocket 实现客户端与服务端的长连接，支持来单提醒和客户催单功能。

测试一下git

测试git：在github中更新。

第二次测试：在远程。
