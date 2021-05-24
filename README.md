<div align="center">

# Awesome Swoole

A curated list of awesome things related to <a href="//github.com/swoole/swoole-src">swoole</a>.

<img src="https://cdn.jsdelivr.net/gh/swoole/swoole-src/mascot.png">

</div>

Table of Contents
=================

   * [Awesome Swoole](#awesome-swoole)
      * [Client Packages](#client-packages)
      * [Cronjobs](#cronjobs)
      * [Database](#database)
      * [Debugging](#debugging)
      * [Development Environment](#development-environment)
      * [Frameworks](#frameworks)
      * [Framework Adapters](#framework-adapters)
      * [Logging](#logging)
      * [Message Queue](#message-queue)
      * [SOA governance](#soa-governance)
      * [Tasks](#tasks)
      * [Third-party SDK](#third-party-sdk)
      * [Miscellaneous](#miscellaneous)
   * [Resources](#resources)
      * [Swoole Videos](#swoole-videos)

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

## Cronjobs

- [hyperf/crontab](https://github.com/hyperf/crontab) - The cron component for Hyperf, allowing jobs to run at intervals of seconds.
- [osgochina/swoole-crontab](https://github.com/osgochina/swoole-crontab) - A Swoole-based crontab schedule. It allows jobs to run at intervals of seconds, and is fully compatible with crontab syntax.

## Database

- [hyperf/database](https://github.com/hyperf/database) - The database component for Hyperf.
- [louislivi/smproxy](https://github.com/louislivi/SMProxy) - SMProxy (Swoole MySQL Proxy), A MySQL database connection pool library.
- [mix-php/database](https://github.com/mix-php/database) - A Swoole-based database component, with built-in support for connection pool.
- [mix-php/redis](https://github.com/mix-php/redis) - A Swoole-based Redis component, with built-in support for connection pool.
- [mix-php/redis-subscribe](https://github.com/mix-php/redis-subscribe) - A Swoole-based Redis subscription component.
- [open-smf/connection-pool](https://github.com/open-smf/connection-pool) - A common connection pool based on Swoole.
- [simple-swoole/db](https://github.com/simple-swoole/db) - The database component of [Simps](https://github.com/simple-swoole/simps). This component is built on top of [the Swoole Library](https://github.com/swoole/library).

## Debugging

- [Swoole Tracker](https://business.swoole.com/tracker/index) - An online service to track and analyze the performances of PHP/Swoole applications. Key features include memory leak detection, performance analytics, and runtime stats. Chinese version only.
- [swoole/debugger](https://github.com/swoole/debugger) - A remote debugger of Swoole. By adding one-line of code, you can debug your application remotely using a rich list of commands.
- [swoole/sdebug](https://github.com/swoole/sdebug) - A fork of [Xdebug](https://github.com/xdebug/xdebug) to debug Swoole applications.
- [upscale/swoole-blackfire](https://github.com/upscalesoftware/swoole-blackfire) - Blackfire profiler integration for Swoole web-server.
- [yasd](https://github.com/swoole/yasd) - Yet Another Swoole Debugger.

## Development Environment

- [phpswoole/swoole](https://github.com/swoole/docker-swoole) - Official Docker Image of Swoole.
- [swoole/ide-helper](https://github.com/swoole/ide-helper) - IDE help files to provide accurate autocompletion for Swoole.

## Frameworks

- [chubbyphp/chubbyphp-framework](https://github.com/chubbyphp/chubbyphp-framework): A minimal middleware based micro framework using PSR, with the goal is to achive the best combination of flexibility and simplicity by using standards.
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
- [imi](https://github.com/Yurunsoft/IMI) - A Swoole-based framework, with built-in support for HTTP/1, HTTP/2, WebSocket, TCP, UDP, and MQTT.
- Laminas/Mezzio/Zend Framework
    - [mezzio/mezzio-swoole](https://github.com/mezzio/mezzio-swoole) - Provides the support of Swoole into a [Mezzio](https://docs.mezzio.dev/) application.
- Laravel
    - [Laravel Octane](https://github.com/laravel/octane) - Laravel Octane supercharges your application's performance by serving your application using high-powered application servers, including Swoole and [RoadRunner](https://roadrunner.dev).
- [lizhichao/one](https://github.com/lizhichao/one) - A simple and efficient framework that works both under PHP-FPM and Swoole.
- [Mix PHP](https://github.com/mix-php/mix) - A single-threaded coroutine PHP framework.
    - [mix-php/database](https://github.com/mix-php/database)
    - [mix-php/monolog](https://github.com/mix-php/monolog)
    - [mix-php/redis](https://github.com/mix-php/redis)
    - [mix-php/redis-subscribe](https://github.com/mix-php/redis-subscribe)
    - [mix-php/tracing-zipkin](https://github.com/mix-php/tracing-zipkin)
    - [mix-php/sync-invoke](https://github.com/mix-php/sync-invoke)
- [phpmv/ubiquity](https://github.com/phpMv/ubiquity) - A powerful and fast framework for efficient design.
- [Simps](https://github.com/simple-swoole/simps) - A simple, lightweight and high-performance PHP coroutine framework.

## Framework Adapters

_To run PHP/PHP-FPM frameworks using Swoole._

- Laravel
    - [swooletw/laravel-swoole](https://github.com/swooletw/laravel-swoole) - A high-performance HTTP server to run Laravel/Lumen application on top of Swoole.
    - [hhxsv5/laravel-s](https://github.com/hhxsv5/laravel-s) - An out-of-the-box adapter to run Laravel/Lumen applications with Swoole.
    - [toxmc/fast-laravel](https://github.com/toxmc/fast-laravel) - A Swoole-based high-performance HTTP server to speed up your Laravel applications.
- Phalcon
    - [phwoolcon/phwoolcon](https://github.com/phwoolcon/phwoolcon) - Phalcon + Swoole.
- Slim
    - [pachico/Slim-Swoole](https://github.com/pachico/slim-swoole) - A convenient library to run [SlimPHP](https://www.slimframework.com) applications with Swoole.
- Symfony
    - [k911/swoole-bundle](https://github.com/k911/swoole-bundle) - Symfony integration with Swoole to speed up your applications.
- YII
    - [liufee/yii2-swoole](https://github.com/liufee/yii2-swoole) - To run [Yii 2](https://www.yiiframework.com) applications with Swoole.

## Logging

- [hyperf/logger](https://github.com/hyperf/logger) - The logging component for Hyperf. It's based on [Monolog](https://github.com/Seldaek/monolog), with PSR-3 interface implemented.
- [mix-php/monolog](https://github.com/mix-php/monolog) - A coroutine-friendly logging library. It's based on [Monolog](https://github.com/Seldaek/monolog).
- [upscale/swoole-newrelic](https://github.com/upscalesoftware/swoole-newrelic) - New Relic APM and Browser monitoring of Swoole web-server.

## Message Queue

- [hyperf/amqp](https://github.com/hyperf/amqp) - The AMQP client for Hyperf.
- [hyperf/async-queue](https://github.com/hyperf/async-queue) - The Redis-based asynchronous queue component for Hyperf.
- [longyan/phpkafka](https://github.com/longyan/phpkafka) - A coroutine-based [Kafka](https://kafka.apache.org) client.

## SOA governance

- [hyperf/tracer](https://github.com/hyperf/tracer) - The distributed tracing component for Hyperf. The implementation is based on [OpenTracing](https://opentracing.io).
- [mix-php/tracing-zipkin](https://github.com/mix-php/tracing-zipkin) - A tracing library based on [Zipkin](https://zipkin.io) and [OpenTracing](https://opentracing.io).

## Tasks

- [hyperf/task](https://github.com/hyperf/task) - The task component for Hyperf, providing an easy way to add and dispatch tasks to task workers in Swoole.
- [kcloze/swoole-jobs](https://github.com/kcloze/swoole-jobs) - An efficient Swoole-based job queue system.

## Third-party SDK

- [Yurunsoft/PaySDK](https://github.com/Yurunsoft/PaySDK) - A coroutine-friendly payment SDK for Alipay and WeChat Pay.
- [Yurunsoft/YurunOAuthLogin](https://github.com/Yurunsoft/YurunOAuthLogin) - An OAuth library that provides built-in support for QQ、WeChat、Weibo、Github、Gitee, etc.

## Miscellaneous

- [leocavalcante/swoole-futures](https://github.com/leocavalcante/swoole-futures) - Futures + Async/Await for PHP's Swoole asynchronous run-time.
- [leocavalcante/swoole-mutex](https://github.com/leocavalcante/swoole-mutex) - Mutual exclusion abstractions for PHP's Swoole concurrency run-time.
- [mix-php/sync-invoke](https://github.com/mix-php/sync-invoke) - A library to execute synchronous blocking code without blocking the running process in Swoole.
- [xlswriter](https://github.com/viest/php-ext-xlswriter) - A coroutine-friendly PHP Extension to create and read XLSX files.

# Resources

## Swoole Videos

Fantastic Swoole-related videos.

- [CSP Programming in PHP](https://nomadphp.com/video/306/csp-programming-in-php)
