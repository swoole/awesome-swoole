<div align="center">

# Awesome Swoole

A curated list of awesome things related to <a href="//github.com/swoole/swoole-src">swoole</a>.

<img src="https://cdn.jsdelivr.net/gh/swoole/swoole-src/mascot.png">

</div>

Table of Contents
=================

* [Awesome Swoole](#awesome-swoole)
    * [Client Packages](#client-packages)
    * [Message Queue](#message-queue)
    * [Database](#database)
    * [Cronjobs](#cronjobs)
    * [Tasks](#tasks)
    * [Debugging](#debugging)
    * [Logging](#logging)
    * [SOA governance](#soa-governance)
    * [Third-party SDK](#third-party-sdk)
    * [Framework](#framework)
    * [Miscellaneous](#miscellaneous)

## Client Packages

- HTTP
    - [Saber](https://github.com/swlib/saber) - A coroutine-based HTTP client.
    - [Yurunsoft/Guzzle-Swoole](https://github.com/Yurunsoft/Guzzle-Swoole) - Make the [Guzzle](https://github.com/guzzle/guzzle) library coroutine-friendly in Swoole. This package supports Guzzle 6 and Guzzle 7. It works with package [elasticsearch/elasticsearch](https://github.com/elastic/elasticsearch-php) (the official PHP client for Elasticsearch), [aws/aws-sdk-php](https://github.com/aws/aws-sdk-php) (official repository of the AWS SDK for PHP), and many Swoole-based frameworks.
    - [Yurunsoft/YurunHttp](https://github.com/Yurunsoft/YurunHttp) - An easy-to-use HTTP client that works with HTTP/1, HTTP/2, and WebSocket protocols. It also supports chained operations, concurrent processing, and connection pool.
- [hyperf/jet](https://github.com/hyperf/jet) - An RPC Client with built-in support for [the JSON-RPC protocol](https://www.jsonrpc.org/). It works with both PHP-FPM and Swoole.
- [hyperf/consul](https://github.com/hyperf/consul) - The [Consul](https://www.consul.io) client for Hyperf.
- [hyperf/elasticsearch](https://github.com/hyperf/elasticsearch) - The [Elasticsearch](https://www.elastic.co/elasticsearch/) client for Hyperf.
- [hyperf/etcd](https://github.com/hyperf/etcd) - The [etcd](https://etcd.io) client for Hyperf.
- MQTT
    - [simps/mqtt](https://github.com/simps/mqtt) - A coroutine-based MQTT client. It supports MQTT version 3.1, 3.1.1, and 5.0.
- [swoole/ext-postgresql](https://github.com/swoole/ext-postgresql) - A Swoole-based PostgreSQL client.
- [swoole/ext-zookeeper](https://github.com/swoole/ext-zookeeper) - A Swoole-based ZooKeeper client.
- [swoole/grpc](https://github.com/swoole/grpc) - An efficient Swoole-based gRPC client.

## Message Queue

- [hyperf/amqp](https://github.com/hyperf/amqp) - The AMQP client for Hyperf.
- [hyperf/async-queue](https://github.com/hyperf/async-queue) - The Redis-based asynchronous queue component for Hyperf.
- [longyan/phpkafka](https://github.com/longyan/phpkafka) - A coroutine-based [Kafka](https://kafka.apache.org) client.

## Database

- [hyperf/database](https://github.com/hyperf/database) - The database component for Hyperf.
- [mix-php/database](https://github.com/mix-php/database) - A Swoole-based database component, with built-in support for connection pool.
- [mix-php/redis](https://github.com/mix-php/redis) - A Swoole-based Redis component, with built-in support for connection pool.
- [mix-php/redis-subscribe](https://github.com/mix-php/redis-subscribe) - A Swoole-based Redis subscription component.
- [simple-swoole/db](https://github.com/simple-swoole/db) - The database component of [Simps](https://github.com/simple-swoole/simps). This component is built on top of [the Swoole Library](https://github.com/swoole/library).

## Cronjobs

- [hyperf/crontab](https://github.com/hyperf/crontab) - The cron component for Hyperf, allowing jobs to run at intervals of seconds.
- [osgochina/swoole-crontab](https://github.com/osgochina/swoole-crontab) - A Swoole-based crontab schedule. It allows jobs to run at intervals of seconds, and is fully compatible with crontab syntax.

## Tasks

- [hyperf/task](https://github.com/hyperf/task) - The task component for Hyperf, providing an easy way to add and dispatch tasks to task workers in Swoole.

## Debugging

- [Swoole Tracker](https://business.swoole.com/tracker/index) - An online service to track and analyze the performances of PHP/Swoole applications. Key features include memory leak detection, performance analytics, and runtime stats. Chinese version only.
- [swoole/debugger](https://github.com/swoole/debugger) - A remote debugger of Swoole. By adding one-line of code, you can debug your application remotely using a rich list of commands.
- [swoole/ide-helper](https://github.com/swoole/ide-helper) - IDE help files to provide accurate autocompletion for Swoole.
- [swoole/sdebug](https://github.com/swoole/sdebug) - A fork of [Xdebug](https://github.com/xdebug/xdebug) to debug Swoole applications.
- [yasd](https://github.com/swoole/yasd) - Yet Another Swoole Debugger.

## Logging

- [hyperf/logger](https://github.com/hyperf/logger) - The logging component for Hyperf. It's based on [Monolog](https://github.com/Seldaek/monolog), with PSR-3 interface implemented.
- [mix-php/monolog](https://github.com/mix-php/monolog) - A coroutine-friendly logging library. It's based on [Monolog](https://github.com/Seldaek/monolog).

## SOA governance

- [hyperf/tracer](https://github.com/hyperf/tracer) - The distributed tracing component for Hyperf. The implementation is based on [OpenTracing](https://opentracing.io).
- [mix-php/tracing-zipkin](https://github.com/mix-php/tracing-zipkin) - A tracing library based on [Zipkin](https://zipkin.io) and [OpenTracing](https://opentracing.io).

## Third-party SDK

- [Yurunsoft/PaySDK](https://github.com/Yurunsoft/PaySDK) - A coroutine-friendly payment SDK for Alipay and WeChat Pay.
- [Yurunsoft/YurunOAuthLogin](https://github.com/Yurunsoft/YurunOAuthLogin) - An OAuth library that provides built-in support for QQ、WeChat、Weibo、Github、Gitee, etc.

## Framework

- [Hyperf](https://github.com/hyperf/hyperf) - A coroutine framework that focuses on hyperspeed and flexibility.
    - Official components (an incomplete list)
        - [hyperf/amqp](https://github.com/hyperf/amqp)
        - [hyperf/async-queue](https://github.com/hyperf/async-queue)
        - [hyperf/consul](https://github.com/hyperf/consul)
        - [hyperf/crontab](https://github.com/hyperf/crontab)
        - [hyperf/database](https://github.com/hyperf/database)
        - [hyperf/elasticsearch](https://github.com/hyperf/elasticsearch)
        - [hyperf/etcd](https://github.com/hyperf/etcd)
        - [hyperf/jet](https://github.com/hyperf/jet)
        - [hyperf/logger](https://github.com/hyperf/logger)
        - [hyperf/task](https://github.com/hyperf/task)
        - [hyperf/tracer](https://github.com/hyperf/tracer)
    - Third-party components (an incomplete list)
        - [96qbhy/hyperf-auth](https://github.com/qbhy/hyperf-auth) - An authentication component for Hyperf. It supports JWT and session-based authentications. You can also create your own authentication drivers if needed.
- Laminas/Mezzio/Zend Framework
    - [mezzio/mezzio-swoole](https://github.com/mezzio/mezzio-swoole) - Provides the support of Swoole into a [Mezzio](https://docs.mezzio.dev/) application.
- Laravel
    - [Laravel Octane](https://github.com/laravel/octane) - Laravel Octane supercharges your application's performance by serving your application using high-powered application servers, including Swoole and [RoadRunner](https://roadrunner.dev).
    - [swooletw/laravel-swoole](https://github.com/swooletw/laravel-swoole) - A Swoole-based high-performance HTTP server to speed up your Laravel/Lumen applications.
    - [hhxsv5/laravel-s](https://github.com/hhxsv5/laravel-s) - An out-of-the-box adapter to run Laravel/Lumen applications with Swoole.
- [Mix PHP](https://github.com/mix-php/mix) - A single-threaded coroutine PHP framework.
    - [mix-php/database](https://github.com/mix-php/database)
    - [mix-php/monolog](https://github.com/mix-php/monolog)
    - [mix-php/redis](https://github.com/mix-php/redis)
    - [mix-php/redis-subscribe](https://github.com/mix-php/redis-subscribe)
    - [mix-php/tracing-zipkin](https://github.com/mix-php/tracing-zipkin)
    - [mix-php/sync-invoke](https://github.com/mix-php/sync-invoke)
- Phalcon
    - [phwoolcon/phwoolcon](https://github.com/phwoolcon/phwoolcon) - Phalcon + Swoole.
- [Simps](https://github.com/simple-swoole/simps) - A simple, lightweight and high-performance PHP coroutine framework.
- Slim
    - [pachico/Slim-Swoole](https://github.com/pachico/slim-swoole) - A convenient library to run [SlimPHP](https://www.slimframework.com) applications with Swoole.
- Symfony
    - [k911/swoole-bundle](https://github.com/k911/swoole-bundle) - Symfony integration with Swoole to speed up your applications.
- YII
    - [liufee/yii2-swoole](https://github.com/liufee/yii2-swoole) - To run [Yii 2](https://www.yiiframework.com) applications with Swoole.

## Miscellaneous

- [mix-php/sync-invoke](https://github.com/mix-php/sync-invoke) - A library to execute synchronous blocking code without blocking the running process in Swoole.
- [xlswriter](https://github.com/viest/php-ext-xlswriter) - A coroutine-friendly PHP Extension to create and read XLSX files.
