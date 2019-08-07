# redislimiter
a distributed limiter based on redis lua script
一个分布式限流熔断工具
## 分布式环境
使用Redis共享令牌数据,通过Lua Script提升Redis访问效率。
## 流量控制
采用令牌桶算法
## 熔断
错误数和错误比例达到设定阀值自动触发熔断。
熔断之后每1分钟释放一个测试信号，测试成功熔断挡板撤销，否则继续熔断。
## 命令模式
可以使用熔断工具同步执行任何程序命令，（后续可支持异步执行）。
## 隔离
不同的目标程序（或者不同的参数目标）限流熔断数据相互隔离，互不影响。

