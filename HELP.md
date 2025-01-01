# 动态数据源Nacos Push模式（v1.8.0）

* sentinel dashboard setRule到Nacos配置中心（需改造sentinel-dashboard模块源码）
* sentinel dashboard 从Nacos配置中心getRule（需改造sentinel-dashboard模块源码）
* sentinel 客户端监听Nacos配置动态加载规则到本地内存（sentinel在sentinel-datasource-nacos包提供了实现，只需引入该依赖，通过配置文件配置源）

## 1、sentinel dashboard setRule到Nacos配置中心
### 改动接口：
com.alibaba.csp.sentinel.dashboard.controller.FlowControllerV1#apiAddFlowRule
