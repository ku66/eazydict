# EazyDict

[![NPM version][npm-image]][npm-url] [![Build Status][travis-image]][travis-url] [![License][license-image]][license-url]

简单易用的命令行词典，基于 Node 开发

特色功能：

- 支持以插件形式集成词典，默认包含: [Google](http://github.com/keenwon/eazydict-google), [Bing](http://github.com/keenwon/eazydict-bing), [Youdao](http://github.com/keenwon/eazydict-youdao)
- 支持本地缓存
- 支持最近查询单词的历史记录
- 支持生词本
- 可查询程序状态（累计查询次数，生词个数等）

目录:
<!-- TOC -->

- [环境](#环境)
- [安装](#安装)
- [运行](#运行)
- [插件](#插件)
- [配置](#配置)
- [License](#license)

<!-- /TOC -->

## 环境

运行 EazyDict 需要 Node(**v6+**)、Npm，安装方法请查看 Node 官网：[https://nodejs.org/](https://nodejs.org/)

## 安装

使用 npm 安装，执行：

```shell
npm i -g eazydict
```

当然也可以使用 [yarn](https://yarnpkg.com)：

```shell
yarn global add eazydict
```

> 注意：因为依赖了 node-sqlite3，会直接根据你的系统下载预编译版本，可能会比较慢，安装时可以添加 `--verbose` 查看详情
>
> ```shell
> npm i -g eazydict --verbose
> ```
> 安装的相关详细信息可以查看: [link](https://github.com/mapbox/node-sqlite3#installing)

## 运行

直接执行 `eazydict` 或者 `eazydict --help` 可以看到详细的帮助信息：

```shell
$ eazydict --help

  Usage: eazydict <words...>

  简单易用的命令行词典 https://github.com/keenwon/eazydict


  Options:

    -s, --save     查询单词，同时保存到生词本
    -V, --version  output the version number
    -h, --help     output usage information


  Commands:

    lookup|l [options] <words...>  查询 words 的翻译
    history|h                      显示最近查询的历史记录
    save|s                         保存上一次查询的单词、短语到生词本
    wordbook|w                     打开生词本
    status                         显示统计信息

  Examples:

    查询短语 "fly in sky"：
    $ eazydict fly in sky
    $ eazydict lookup fly in sky
    $ eazydict l fly in sky

    查询短语 "hello"，同时保存到生词本：
    $ eazydict --save hello
    $ eazydict -s hello

    查看历史记录：
    $ eazydict history
    $ eazydict h

    保存上一次查询的单词、短语到生词本：
    $ eazydict save
    $ eazydict s

    打开生词本：
    $ eazydict wordbook
    $ eazydict w

    查看 EazyDict 版本信息:
    $ eazydict -V
    $ eazydict --version
```

## 插件

- [eazydict-google](http://github.com/keenwon/eazydict-google) (默认包含，无需安装)
- [eazydict-bing](http://github.com/keenwon/eazydict-bing) (默认包含，无需安装)
- [eazydict-youdao](http://github.com/keenwon/eazydict-youdao) (默认包含，无需安装)

## 配置

TODO

## License

MIT.

[npm-image]: https://img.shields.io/npm/v/eazydict.svg?style=flat-square
[npm-url]: https://www.npmjs.com/package/eazydict
[travis-image]: https://img.shields.io/travis/keenwon/eazydict.svg?style=flat-square
[travis-url]: https://travis-ci.org/keenwon/eazydict
[license-image]: https://img.shields.io/npm/l/express.svg?style=flat-square
[license-url]: https://github.com/keenwon/eazydict/blob/master/LICENSE