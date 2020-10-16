<div align="center">

# Awesome Swoole

A curated list of awesome things related to <a href="//github.com/swoole/swoole-src">swoole</a>.

<img src="https://cdn.jsdelivr.net/gh/swoole/swoole-src/mascot.png">

</div>

## 客户端

- [swoole/grpc](https://github.com/swoole/grpc) 由 Swoole 驱动的 Grpc 协程客户端, 底层使用高性能协程 Http2-Client 客户端
- [swoole/ext-zookeeper](https://github.com/swoole/ext-zookeeper) 基于 Swoole 协程的 PHP ZooKeeper 客户端
- [swoole/ext-postgresql](https://github.com/swoole/ext-postgresql) 基于 Swoole 协程的 PHP PostgreSQL 客户端
- [swlib/saber](https://github.com/swlib/saber) PHP异步协程HTTP客户端
- [hyperf/jet](https://github.com/hyperf/jet) 一个统一模型的 RPC 客户端，内置 JSONRPC 协议的适配，该组件可适用于所有的 PHP 环境，包括 PHP-FPM 和 Swoole
- [hyperf/consul](https://github.com/hyperf/consul) 由 Hyperf 提供的 Consul 协程客户端
- [hyperf/elasticsearch](https://github.com/hyperf/elasticsearch) 由 Hyperf 提供的 Elasticsearch 协程客户端
- [hyperf/etcd](https://github.com/hyperf/etcd) 由 Hyperf 提供的 ETCD 协程客户端
- [Yurunsoft/Guzzle-Swoole](https://github.com/Yurunsoft/Guzzle-Swoole) 让基于 Guzzle 的项目完美无缝兼容 Swoole 协程，支持：Guzzle、Elasticsearch Client
- [Yurunsoft/YurunHttp](https://github.com/Yurunsoft/YurunHttp) 完美支持Curl、Swoole 协程的 PHP HTTP 客户端，支持链式操作，简单易用
- [viest/php-ext-xlswriter](https://github.com/viest/php-ext-xlswriter) 支持 Swoole 协程环境，可用于在 Excel 2007+ XLSX 文件中读取数据，插入多个工作表，写入文本、数字、公式、日期、图表、图片和超链接
- [louislivi/SMProxy](https://github.com/louislivi/SMProxy) 一个基于 MySQL 协议，Swoole 开发的 MySQL 数据库连接池

## 消息队列

- [Littlesqx/aint-queue](https://github.com/Littlesqx/aint-queue) 基于 Swoole 的一个异步队列库，可弹性伸缩的工作进程池，工作进程协程支持
- [hyperf/amqp](https://github.com/hyperf/amqp) 由 Hyperf 提供的 AMQP 协程组件
- [hyperf/async-queue](https://github.com/hyperf/async-queue) 由 Hyperf 提供的简单的基于 Redis 的异步队列组件

## Crontab

- [osgochina/swoole-crontab](https://github.com/osgochina/swoole-crontab) 基于 Swoole 的定时器程序，支持秒级处理，完全兼容 Crontab 语法
- [hyperf/crontab](https://github.com/hyperf/crontab) 由 Hyperf 提供的秒级定时任务组件

## Task

- [swlib/archer](https://github.com/swlib/archer) 基于协程Swoole的Task组件，支持多种模式。轻松实现协程Task的队列、并发、Defer、计时器等
- [hyperf/task](https://github.com/hyperf/task) 由 Hyperf 提供的 Task 组件，对 Swoole 的 Task 机制进行了封装及抽象，提供便捷的注解用法

## 热更新

- [mix-php/swoolefor](https://github.com/mix-php/swoolefor) 一个由 Mixphp 实现的通用热更新组件

## 开发调试

- [swoole/sdebug](https://github.com/swoole/sdebug) 用于协助开发与调试，xdebug 的协程改造版
- [swoole/ide-helper](https://github.com/swoole/ide-helper) 用于在 IDE 中自动补全
- [Swoole Tracker](https://business.swoole.com/tracker.html) 提供内存泄漏分析、阻塞检测、性能分析、运行状态及调用统计等功能

## 第三方 SDK

- [Yurunsoft/PaySDK](https://github.com/Yurunsoft/PaySDK) 支持 Swoole 协程的支付宝/微信支付 SDK
- [Yurunsoft/YurunOAuthLogin](https://github.com/Yurunsoft/YurunOAuthLogin) 支持 Swoole 协程的第三方登录授权 SDK（QQ、微信、微博、Github、Gitee 等）
