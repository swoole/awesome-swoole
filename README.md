<div align="center">

# Awesome Swoole [![Twitter](https://badgen.net/badge/icon/twitter?icon=twitter&label)](https://twitter.com/phpswoole) [![Discord](https://badgen.net/badge/icon/discord?icon=discord&label)](https://discord.swoole.dev) ![](https://github.com/swoole/awesome-swoole/workflows/Awesome%20Bot/badge.svg) [![license](https://img.shields.io/github/license/swoole/awesome-swoole.svg?maxAge=2592000)]()

A curated list of awesome things related to <a href="//github.com/swoole/swoole-src">Swoole</a>.

<img width="200" height="120" align=center alt="Swoole Logo" src="https://cdn.jsdelivr.net/gh/sy-records/staticfile/images/swoole/logo.png">

</div>

Table of Contents
=================

   * [Awesome Swoole](#awesome-swoole-)
      * [Client Packages](#client-packages)
      * [Cronjobs](#cronjobs)
      * [Database](#database)
      * [Debugging and Profiling](#debugging-and-profiling)
      * [Development Environment](#development-environment)
      * [Distribution](#distribution)
      * [Frameworks](#frameworks)
      * [Framework Integration](#framework-integration)
      * [gRPC](#grpc)
      * [HTTP](#http)
      * [Logging](#logging)
      * [Serverless](#serverless)
      * [SOA governance](#soa-governance)
      * [Tasks and Queues](#tasks-and-queues)
      * [Testing](#testing)
      * [Third-party SDK](#third-party-sdk)
      * [Miscellaneous](#miscellaneous)
   * [Resources](#resources)
      * [Best Practices and Use Cases](#best-practices-and-use-cases)
      * [Swoole Books](#swoole-books)
      * [Swoole Videos](#swoole-videos)
      * [Miscellaneous](#miscellaneous-1)

NOTE: Projects labelled with emoji :globe_with_meridians: have their documentation written in non-English languages.

## Client Packages

- [hyperf/jet](https://github.com/hyperf/jet) - An RPC Client with built-in support for [the JSON-RPC protocol](https://www.jsonrpc.org/). It works with both PHP-FPM and Swoole.
- [hyperf/consul](https://github.com/hyperf/consul) - The [Consul](https://www.consul.io) client of Hyperf.
- [hyperf/elasticsearch](https://github.com/hyperf/elasticsearch) - The [Elasticsearch](https://www.elastic.co/elasticsearch/) client of Hyperf.
- [hyperf/etcd](https://github.com/hyperf/etcd) - The [etcd](https://etcd.io) client of Hyperf.
- [simps/mqtt](https://github.com/simps/mqtt) - A coroutine-based MQTT client. It supports MQTT version 3.1, 3.1.1, and 5.0.
- [swoole/ext-postgresql](https://github.com/swoole/ext-postgresql) - A Swoole-based PostgreSQL client.
- [swoole/ext-zookeeper](https://github.com/swoole/ext-zookeeper) - A Swoole-based ZooKeeper client. :globe_with_meridians:

## Cronjobs

- [hyperf/crontab](https://github.com/hyperf/crontab) - The cron component of Hyperf, allowing jobs to run at intervals of seconds.
- [osgochina/swoole-crontab](https://github.com/osgochina/swoole-crontab) - A Swoole-based crontab schedule. It allows jobs to run at intervals of seconds, and is fully compatible with crontab syntax. :globe_with_meridians:

## Database

- [hyperf/database](https://github.com/hyperf/database) - The database component of Hyperf.
- [mix/database](https://github.com/mix-php/database) - A Swoole-based database component, with built-in support for connection pool. :globe_with_meridians:
- [mix/redis](https://github.com/mix-php/redis) - A Swoole-based Redis component, with built-in support for connection pool. :globe_with_meridians:
- [mix/redis-subscriber](https://github.com/mix-php/redis-subscriber) - A Swoole-based Redis subscription component. :globe_with_meridians:
- [open-smf/connection-pool](https://github.com/open-smf/connection-pool) - A common connection pool based on Swoole.
- [simple-swoole/db](https://github.com/simple-swoole/db) - The database component of [Simps](https://github.com/simple-swoole/simps). This component is built on top of [the Swoole Library](https://github.com/swoole/library).
- [SMProxy](https://github.com/louislivi/SMProxy) - SMProxy (Swoole MySQL Proxy), A MySQL database connection pool library. :globe_with_meridians:

## Debugging and Profiling

- [SkyAPM PHP](https://github.com/SkyAPM/SkyAPM-php-sdk) - The PHP instrument agent for [Apache SkyWalking](https://skywalking.apache.org).
- [Swoole Tracker](https://business.swoole.com/tracker/index) - An online service to track and analyze the performances of PHP/Swoole applications. Key features include memory leak detection, performance analytics, and runtime stats. Chinese version only. :globe_with_meridians:
- [swoole/debugger](https://github.com/swoole/debugger) - A remote debugger of Swoole. By adding one-line of code, you can debug your application remotely using a rich list of commands. :globe_with_meridians:
- [upscale/swoole-blackfire](https://github.com/upscalesoftware/swoole-blackfire) - Blackfire profiler integration for Swoole web-server.
- [yasd](https://github.com/swoole/yasd) - Yet Another Swoole Debugger, developed by [codinghuang](https://github.com/huanghantao) from the Swoole team.

## Development Environment

- Docker
    - [phpswoole/swoole](https://github.com/swoole/docker-swoole) - Official Docker image of Swoole.
- IDE Helper
    - [eaglewu/swoole-ide-helper](https://github.com/wudi/swoole-ide-helper) - Auto completion, trigger suggest and view docs for Swoole in editor.
    - [Swoole IDE Helper](https://plugins.jetbrains.com/plugin/13040-swoole-ide-helper) - Swoole IDE Helper for PhpStorm and Intellij IDEA. Thanks to [Luhur Abdi (Abi) Rizal](https://elabee.me) for maintaining it.
    - [swoole/ide-helper](https://github.com/swoole/ide-helper) - IDE help files to provide accurate autocompletion for Swoole.

## Distribution

- [static-php-cli](https://github.com/crazywhalecc/static-php-cli) - Build static PHP binary in Linux, with Swoole and other popular extensions included. :globe_with_meridians:

## Frameworks

- [chubbyphp-framework](https://github.com/chubbyphp/chubbyphp-framework): A minimal middleware based micro framework using PSR, with the goal is to achive the best combination of flexibility and simplicity by using standards.
- [Hyperf](https://github.com/hyperf/hyperf) - A coroutine framework that focuses on hyperspeed and flexibility.
    - Official components (an incomplete list)
        - [hyperf/amqp](https://github.com/hyperf/amqp)
        - [hyperf/async-queue](https://github.com/hyperf/async-queue)
        - [hyperf/consul](https://github.com/hyperf/consul)
        - [hyperf/crontab](https://github.com/hyperf/crontab)
        - [hyperf/database](https://github.com/hyperf/database)
        - [hyperf/elasticsearch](https://github.com/hyperf/elasticsearch)
        - [hyperf/etcd](https://github.com/hyperf/etcd)
        - [hyperf/filesystem](https://github.com/hyperf/filesystem)
        - [hyperf/jet](https://github.com/hyperf/jet)
        - [hyperf/logger](https://github.com/hyperf/logger)
        - [hyperf/task](https://github.com/hyperf/task)
        - [hyperf/tracer](https://github.com/hyperf/tracer)
    - Third-party components (an incomplete list)
        - [96qbhy/hyperf-auth](https://github.com/qbhy/hyperf-auth) - An authentication component for Hyperf. It supports JWT and session-based authentications. You can also create your own authentication drivers if needed.
        - [reasno/fastmongo](https://github.com/Reasno/fastmongo) - A coroutine-based MongoDB client for Hyperf.
        - [leocavalcante/hyperf-doctrine](https://github.com/leocavalcante/hyperf-doctrine) - This project provides an integration for the Doctrine ORM and the Hyperf framework.
- [Nano](https://github.com/hyperf/nano) - A Hyperf-based coroutine microframework.
- [imi](https://github.com/imiphp/imi) - A Swoole-based framework, with built-in support for HTTP/1, HTTP/2, WebSocket, TCP, UDP, and MQTT. :globe_with_meridians:
- Laminas/Mezzio/Zend Framework
    - [mezzio/mezzio-swoole](https://github.com/mezzio/mezzio-swoole) - Provides the support of Swoole into a [Mezzio](https://docs.mezzio.dev/) application.
- [Siler](https://github.com/leocavalcante/siler) - A set of general purpose high-level abstractions aiming an API for declarative programming in PHP.
- [lizhichao/one](https://github.com/lizhichao/one) - A simple and efficient framework that works both under PHP-FPM and Swoole.
- [Mix PHP](https://github.com/mix-php/mix) - A unique single-threaded coroutine-based framework. :globe_with_meridians:
    - Official modules (an incomplete list)
        - [mix/database](https://github.com/mix-php/database)
        - [mix/monolog](https://github.com/mix-php/monolog)
        - [mix/redis](https://github.com/mix-php/redis)
        - [mix/redis-subscriber](https://github.com/mix-php/redis-subscriber)
        - [mix/tracing-zipkin](https://github.com/mix-php/tracing-zipkin)
        - [mix/sync-invoke](https://github.com/mix-php/sync-invoke)
- [Polyel](https://github.com/Superbition/Polyel-Framework) - A full-stack MVC PHP framework/server built from the ground up based on Swoole.
- [QueryPHP](https://www.queryphp.com) - A modern, high performance PHP progressive coroutine framework. :globe_with_meridians:
- [Simps](https://github.com/simple-swoole/simps) - A simple, lightweight and high-performance PHP coroutine framework.
- [Ubiquity](https://github.com/phpMv/ubiquity) - A powerful and fast framework for efficient design.

## Framework Integration
*To run PHP/PHP-FPM frameworks using Swoole.*

- [PHP Runtimes](https://github.com/php-runtime/runtime) - A home for runtimes, where people can easily create a `Runtime` to run an application with Bref, Swoole or ReactPHP without making any change to the application itself.
- Laravel
    - [Laravel Octane](https://github.com/laravel/octane) - A first-party Laravel package that supercharges laravelish application's performance by serving it using Swoole high-performance HTTP servers. Developed and maintained by the Laravel team.
    - [hhxsv5/laravel-s](https://github.com/hhxsv5/laravel-s) - Glue for using Swoole in Laravel or Lumen.
    - [huang-yi/shadowfax](https://github.com/huang-yi/shadowfax) - Runs your Laravel application on Swoole.
    - [scil/laravel-fly](https://github.com/scil/LaravelFly) - To be an absolutely safe solution to speed up Laravel with Swoole. Preloading + Coroutine and Tinker Online.
    - [swooletw/laravel-swoole](https://github.com/swooletw/laravel-swoole) - A high-performance HTTP server to run Laravel/Lumen application on top of Swoole.
    - [toxmc/fast-laravel](https://github.com/toxmc/fast-laravel) - A Swoole-based high-performance HTTP server to speed up your Laravel applications. :globe_with_meridians:
- Phalcon
    - [phwoolcon/phwoolcon](https://github.com/phwoolcon/phwoolcon) - Phalcon + Swoole.
- Slim
    - [pachico/Slim-Swoole](https://github.com/pachico/slim-swoole) - A convenient library to run [SlimPHP](https://www.slimframework.com) applications with Swoole.
- Symfony
    - [symfony/runtime](https://github.com/symfony/runtime) - The Runtime component decouples the bootstrapping logic from any global state to make sure the application can run with runtimes like PHP-FPM, ReactPHP, Swoole, etc. without any changes. For a more generic implementation that works with other frameworks/environments, please check project [PHP Runtimes](https://github.com/php-runtime/runtime).
    - [k911/swoole-bundle](https://github.com/k911/swoole-bundle) - Symfony integration with Swoole to speed up your applications.
- ThinkPHP
    - [topthink/think-swoole](https://github.com/top-think/think-swoole) - To run ThinkPHP applications with Swoole. :globe_with_meridians:
- Yii
    - [liufee/yii2-swoole](https://github.com/liufee/yii2-swoole) - To run [Yii 2](https://www.yiiframework.com) applications with Swoole. :globe_with_meridians:
- [Utopia](https://github.com/utopia-php/framework)
    - [Utopia Swoole](https://github.com/utopia-php/swoole) - An extension for Utopia Framework to work with PHP Swoole as a PHP FPM alternative.

## gRPC

- [hyperf/grpc-client](https://github.com/hyperf/grpc-client) - The gRPC client component of Hyperf.
- [hyperf/grpc-server](https://github.com/hyperf/grpc-server) - The gRPC server component of Hyperf.
- [mix/grpc](https://github.com/mix-php/grpc) - A gRPC implementation based on Swoole. Protoc code generator, server, client, and more features included. :globe_with_meridians:
- [swoole/grpc](https://github.com/swoole/grpc) - An efficient Swoole-based gRPC client. :globe_with_meridians:

## HTTP
*Libraries for working with HTTP.*

- PSR Compliance
    - [chubbyphp/chubbyphp-swoole-request-handler](https://github.com/chubbyphp/chubbyphp-swoole-request-handler) - A request handler adapter for Swoole, using PSR-7, PSR-15 and PSR-17.
    - [leocavalcante/request-callback](https://github.com/leocavalcante/request-callback) - Swoole request callback for PSR compliant handlers. Compatible with PSR-7 and PSR-15.
    - [fastd/http](https://github.com/fastdlabs/http) - A PSR-7-compatible HTTP component, with built-in support for Swoole HTTP server. :globe_with_meridians:
- [Saber](https://github.com/swlib/saber) - A coroutine-based HTTP client. :globe_with_meridians:
- [Yurunsoft/Guzzle-Swoole](https://github.com/Yurunsoft/Guzzle-Swoole) - Make the [Guzzle](https://github.com/guzzle/guzzle) library coroutine-friendly in Swoole. It works with many Guzzle-based packages and Swoole-based frameworks. :globe_with_meridians:
- [Yurunsoft/YurunHttp](https://github.com/Yurunsoft/YurunHttp) - An easy-to-use HTTP client that works with HTTP/1, HTTP/2, and WebSocket protocols. It also supports chained operations, concurrent processing, and connection pool. :globe_with_meridians:

## Logging

- [hyperf/logger](https://github.com/hyperf/logger) - The logging component of Hyperf. It's based on [Monolog](https://github.com/Seldaek/monolog), with PSR-3 interface implemented.
- [mix/monolog](https://github.com/mix-php/monolog) - A coroutine-friendly logging library. It's based on [Monolog](https://github.com/Seldaek/monolog). :globe_with_meridians:
- [upscale/swoole-newrelic](https://github.com/upscalesoftware/swoole-newrelic) - New Relic APM and Browser monitoring of Swoole web-server.

## Serverless

- [Swoole Runtime for AWS Lambda](https://github.com/leocavalcante/aws-lambda-swoole-runtime) - λ Run PHP Coroutines & Fibers as-a-Service on the AWS Lambda.

## SOA governance

- [hyperf/tracer](https://github.com/hyperf/tracer) - The distributed tracing component of Hyperf. The implementation is based on [OpenTracing](https://opentracing.io).
- [mix/tracing-zipkin](https://github.com/mix-php/tracing-zipkin) - A tracing library based on [Zipkin](https://zipkin.io) and [OpenTracing](https://opentracing.io). :globe_with_meridians:

## Tasks and Queues

- [Archer](https://github.com/swlib/archer) - A Swoole-based task component, with different runtime modes supported: serial queue, concurrent queue, defer, timer, etc. :globe_with_meridians:
- [hyperf/amqp](https://github.com/hyperf/amqp) - The AMQP client of Hyperf.
- [hyperf/async-queue](https://github.com/hyperf/async-queue) - The Redis-based asynchronous queue component of Hyperf.
- [hyperf/task](https://github.com/hyperf/task) - The task component of Hyperf, providing an easy way to add and dispatch tasks to task workers in Swoole.
- [kcloze/swoole-jobs](https://github.com/kcloze/swoole-jobs) - An efficient Swoole-based job queue system. :globe_with_meridians:
- [littlesqx/aint-queue](https://github.com/Littlesqx/aint-queue) - An async-queue library built on top of Swoole.
- [longlang/phpkafka](https://github.com/swoole/phpkafka) - A coroutine-based [Kafka](https://kafka.apache.org) client.

## Testing

- [deminy/counit](https://github.com/deminy/counit) - To run time/IO related unit tests (e.g., sleep function calls, database queries, API calls, etc) faster using Swoole.

## Third-party SDK

- [yansongda/pay](https://github.com/yansongda/pay) - A payment SDK for Alipay and WeChat Pay, with components to integrate with [Hyperf](https://github.com/yansongda/hyperf-pay), [Laravel](https://github.com/yansongda/laravel-pay), and [Yii](https://github.com/guanguans/yii-pay). :globe_with_meridians:
- [Yurunsoft/PaySDK](https://github.com/Yurunsoft/PaySDK) - A coroutine-friendly payment SDK for Alipay and WeChat Pay. :globe_with_meridians:
- [Yurunsoft/YurunOAuthLogin](https://github.com/Yurunsoft/YurunOAuthLogin) - An OAuth library that provides built-in support for QQ, WeChat, Weibo, Github, Gitee, etc. :globe_with_meridians:

## Miscellaneous

- [crowdstar/exponential-backoff](https://github.com/Crowdstar/exponential-backoff) - A library to prevent overloading an unavailable service by doubling the timeout each iteration. It works under both Swoole (in non-blocking mode) and PHP-FPM.
- [k8s/client](https://github.com/k8s-client/client) - A Kubernetes API client for PHP.
- [leocavalcante/swoole-futures](https://github.com/leocavalcante/swoole-futures) - Futures + Async/Await for PHP's Swoole asynchronous run-time.
- [leocavalcante/swoole-mutex](https://github.com/leocavalcante/swoole-mutex) - Mutual exclusion abstractions for PHP's Swoole concurrency run-time.
- [mix/sync-invoke](https://github.com/mix-php/sync-invoke) - A library to execute synchronous blocking code without blocking the running process in Swoole. :globe_with_meridians:
- [xlswriter](https://github.com/viest/php-ext-xlswriter) - A coroutine-friendly PHP Extension to create and read XLSX files.
- [yurun-crawler](https://github.com/Yurunsoft/yurun-crawler) - A framework to build high-performance, distributed web crawler. :globe_with_meridians:
- [swoole-utils](https://github.com/apinstein/swoole-utils) - A collection of utilities for building concurrent applications with Swoole. **#WIP**

# Resources

## Best Practices and Use Cases

* [Buggregator](https://github.com/buggregator/app) - A beautiful, lightweight debug server that helps you debug your app. Built with Laravel and Swoole.

## Swoole Books
*Fantastic Swoole-related books.*

- [Mastering Swoole PHP](https://www.amazon.com/Mastering-Swoole-PHP-performance-concurrent-ebook/dp/B0881B227S/) - Build your high performance large scale concurrent system in a more flexible and efficient way than ever before with this first & only Swoole PHP book, with PHP 8 ready.

## Swoole Videos
*Fantastic Swoole-related videos.*

- [CSP Programming in PHP](https://nomadphp.com/video/306/csp-programming-in-php) - An online talk presented by Demin on August 20, 2020. This talk gives an in depth explanation on the concurrency model used in Swoole. [Here](http://talks.deminy.in/csp.html) are the slides.
- [Building High-Performance Application Servers with Swoole](https://www.youtube.com/watch?v=fVdDB4mbGYQ) - A conference talk presented by Demin during PHPFest 2020. [Here](http://talks.deminy.in/phpfest2020.html) are the slides.
- [Build an All-In-One Application Server Using Swoole](https://www.youtube.com/watch?v=SJPZxvEYXxI&t=1255s) - A conference talk presented by Demin during PHP Community Summit 2021. The talk starts at 20'55''. [Here](http://talks.deminy.in/pcs21.html) are the slides.

## Miscellaneous

- [deminy/swoole-by-examples](https://github.com/deminy/swoole-by-examples) - Learn Swoole by examples.
- [swooletw/awesome-swoole](https://github.com/swooletw/awesome-swoole) - A curated list of Swoole.
