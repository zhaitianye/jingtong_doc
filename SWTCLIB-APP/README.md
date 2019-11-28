# swtclib_app

> 作为swtc-lib处理的中间层,提供 RESTFul API 接口服务

## 目录

<!-- TOC -->

- [swtclib_app](#swtclib_app)
  - [目录](#目录)
  - [启动服务](#启动服务)
    - [运行环境](#运行环境)
    - [项目发布](#项目发布)
    - [项目停止](#项目停止)
    - [项目更新](#项目更新)
    - [日志文件目录](#日志文件目录)
  - [接口文档](#接口文档)
    - [说明](#说明)
    - [3.1 创建钱包](#31-创建钱包)
      - [类型](#类型)
      - [描述](#描述)
      - [参数说明](#参数说明)
      - [请求地址](#请求地址)
      - [cURL](#curl)
      - [返回值示例](#返回值示例)
      - [返回值解析](#返回值解析)
    - [3.2 根据私钥创建钱包](#32-根据私钥创建钱包)
      - [类型](#类型-1)
      - [描述](#描述-1)
      - [参数说明](#参数说明-1)
        - [参数介绍](#参数介绍)
        - [参数示例](#参数示例)
      - [请求地址](#请求地址-1)
      - [cURL](#curl-1)
      - [返回值示例](#返回值示例-1)
      - [返回值解析](#返回值解析-1)
    - [4.2 创建连接获取服务器基础信息](#42-创建连接获取服务器基础信息)
      - [类型](#类型-2)
      - [描述](#描述-2)
      - [参数说明](#参数说明-2)
      - [请求地址](#请求地址-2)
      - [cURL](#curl-2)
      - [返回值示例](#返回值示例-2)
      - [返回值解析](#返回值解析-2)
    - [4.4 请求底层服务器信息](#44-请求底层服务器信息)
      - [类型](#类型-3)
      - [描述](#描述-3)
      - [参数说明](#参数说明-3)
      - [请求地址](#请求地址-3)
      - [cURL](#curl-3)
      - [返回值示例](#返回值示例-3)
      - [返回值解析](#返回值解析-3)
    - [4.5 获取最新账本信息](#45-获取最新账本信息)
      - [类型](#类型-4)
      - [描述](#描述-4)
      - [参数说明](#参数说明-4)
      - [请求地址](#请求地址-4)
      - [cURL](#curl-4)
      - [返回值示例](#返回值示例-4)
      - [返回值解析](#返回值解析-4)
    - [4.6.1 根据hash获取某一账本具体信息](#461-根据hash获取某一账本具体信息)
      - [类型](#类型-5)
      - [描述](#描述-5)
      - [请求地址](#请求地址-5)
      - [参数说明](#参数说明-5)
        - [参数介绍](#参数介绍-1)
      - [cURL](#curl-5)
      - [返回值示例](#返回值示例-5)
      - [返回值解析](#返回值解析-5)
    - [4.6.2 根据账本高度获取某一账本具体信息](#462-根据账本高度获取某一账本具体信息)
      - [类型](#类型-6)
      - [描述](#描述-6)
      - [请求地址](#请求地址-6)
      - [参数说明](#参数说明-6)
        - [参数介绍](#参数介绍-2)
      - [cURL](#curl-6)
      - [返回值示例](#返回值示例-6)
      - [返回值解析](#返回值解析-6)
    - [4.7 查询某一交易具体信息](#47-查询某一交易具体信息)
      - [类型](#类型-7)
      - [描述](#描述-7)
      - [请求地址](#请求地址-7)
      - [参数说明](#参数说明-7)
        - [参数介绍](#参数介绍-3)
      - [cURL](#curl-7)
      - [返回值示例](#返回值示例-7)
      - [返回值解析](#返回值解析-7)
    - [4.8.1 请求账号信息](#481-请求账号信息)
      - [类型](#类型-8)
      - [描述](#描述-8)
      - [请求地址](#请求地址-8)
      - [参数说明](#参数说明-8)
        - [参数介绍](#参数介绍-4)
      - [cURL](#curl-8)
      - [返回值示例](#返回值示例-8)
      - [返回值解析](#返回值解析-8)
    - [4.8.2 请求余额](#482-请求余额)
      - [类型](#类型-9)
      - [描述](#描述-9)
      - [请求地址](#请求地址-9)
      - [参数说明](#参数说明-9)
        - [参数介绍](#参数介绍-5)
      - [cURL](#curl-9)
      - [返回值示例](#返回值示例-9)
      - [返回值解析](#返回值解析-9)
    - [4.12 获得账号交易列表](#412-获得账号交易列表)
      - [类型](#类型-10)
      - [描述](#描述-10)
      - [请求地址](#请求地址-10)
      - [参数说明](#参数说明-10)
        - [参数介绍](#参数介绍-6)
      - [cURL](#curl-10)
      - [返回值示例](#返回值示例-10)
      - [返回值解析](#返回值解析-10)
    - [4.15.1 单笔支付](#4151-单笔支付)
      - [类型](#类型-11)
      - [描述](#描述-11)
      - [请求地址](#请求地址-11)
      - [参数说明](#参数说明-11)
        - [参数介绍](#参数介绍-7)
        - [参数示例](#参数示例-1)
      - [cURL](#curl-11)
      - [返回值示例](#返回值示例-11)
      - [返回值解析](#返回值解析-11)
    - [4.15.2 需要sequence的串行批量支付](#4152-需要sequence的串行批量支付)
      - [类型](#类型-12)
      - [描述](#描述-12)
      - [请求地址](#请求地址-12)
      - [参数说明](#参数说明-12)
        - [参数介绍](#参数介绍-8)
        - [参数示例](#参数示例-2)
      - [cURL](#curl-12)
      - [返回值示例](#返回值示例-12)
      - [返回值解析](#返回值解析-12)
    - [4.15.3 不需要sequence的串行批量支付](#4153-不需要sequence的串行批量支付)
      - [类型](#类型-13)
      - [描述](#描述-13)
      - [请求地址](#请求地址-13)
      - [参数说明](#参数说明-13)
        - [参数介绍](#参数介绍-9)
        - [参数示例](#参数示例-3)
      - [cURL](#curl-13)
      - [返回值示例](#返回值示例-13)
      - [返回值解析](#返回值解析-13)
    - [4.25 监听事件](#425-监听事件)
      - [使用说明](#使用说明)
      - [代码示例](#代码示例)
      - [可执行代码样例Exampl](#可执行代码样例exampl)
      - [返回值](#返回值)
  - [附录](#附录)
    - [附录1:返回值Code说明](#附录1返回值code说明)

<!-- /TOC -->

## 启动服务

### 运行环境

* git 环境
* nodejs -v12.13.0
* yarn
* reids 数据库(如搭建负载均衡需要连接同一台reids数据库服务器)

### 项目发布

* 到linux上找一个空文件夹，逐条运行下面命令

```bash

// 克隆项目,需要克隆主分支
文档暂时不提供克隆办法

// 进入项目文件夹
cd swtclib-app

// 安装依赖
yarn

// 配置发布版本的配置
复制文件 config/config.dev.js -> 更改名称为 config/config.prod.js

// 配置 Redis 数据库
vim config.prod.js
--------更改以下配置----------
config.io = {
    redis: {
        host: '127.0.0.1',
        port: 6379,
        auth_pass: null,
        db: 0,
    },
};
----------------------------
保存

// 启动项目，后面端口号可以自定义
yarn start --port 7900

```

### 项目停止

```bash

// 进入项目文件夹
cd /xxx/xxx/swtclib-app

// 停止项目
yarn stop

```

### 项目更新

```bash

// 进入项目文件夹
cd /xxx/xxx/swtclib-app

// 更新项目
git pull

// 重启项目
yarn stop

// 重启项目，后面端口号可以自定义
yarn start --port 7900

```

### 日志文件目录

> /root/logs/swtclib_app/prod/


## 接口文档

### 说明
此系统基于 [SWTC-LIB](https://github.com/swtcca/swtclib/tree/master/docs/swtclib),文档编号按照 SWTC-LIB 定义的完善。

测试已经部署完毕的服务器地址：http://39.108.227.152:7901
请用此地址做测试使用

### 3.1 创建钱包

#### 类型 

GET 

#### 描述

返回创建的钱包

#### 参数说明

无

#### 请求地址
```
{{host}}/swtclib/wallet/generate
```
#### cURL

```curl
curl --location --request GET "{{host}}/swtclib/wallet/generate"
```
#### 返回值示例

```JSON
{
    "success": true,
    "msg": "成功",
    "code": 0,
    "data": {
        "secret": "snXXXXXXXXXXXXXXXXXXXXXXXXXXX",
        "address": "jNaEyRyQZiGp7wtHoo5xmXngQWS3noeVrD"
    }
}
```
#### 返回值解析

| 参数         | 类型    | 说明                   |
|--------------|---------|----------------------|
| success      | Boolean | 此次请求是否成功       |
| msg          | String  | 返回的信息             |
| code         | Integer | 服务器返回的请求状态码 |
| data         | Object  | SWTC-LIB 返回的数据    |
| data.secret  | String  | 井通钱包私钥           |
| data.address | String  | 井通钱包地址           |

### 3.2 根据私钥创建钱包

#### 类型 

POST 

#### 描述

根据私钥返回创建钱包的地址

#### 参数说明

##### 参数介绍

| 参数   | 类型   | 说明           |
|--------|--------|--------------|
| secret | String | 钱包地址的私钥 |

##### 参数示例

```JSON
{
  "secret":"snXXXXXXXXXXXXXXXXXXXXXXXXXXX",
}
```

#### 请求地址
```
{{host}}/swtclib/wallet/generate
```
#### cURL

```curl
curl --location --request POST "{{host}}/swtclib/wallet/generate" \
--header "Content-Type: application/x-www-form-urlencoded" \
--data "secret=snXXXXXXXXXXXXXXXXXXXXXXXXXXX"
```
#### 返回值示例

```JSON
{
    "success": true,
    "msg": "成功",
    "code": 0,
    "data": {
        "secret": "snXXXXXXXXXXXXXXXXXXXXXXXXXXX",
        "address": "jNaEyRyQZiGp7wtHoo5xmXngQWS3noeVrD"
    }
}
```
#### 返回值解析

| 参数         | 类型    | 说明                   |
|--------------|---------|----------------------|
| success      | Boolean | 此次请求是否成功       |
| msg          | String  | 返回的信息             |
| code         | Integer | 服务器返回的请求状态码 |
| data         | Object  | SWTC-LIB 返回的数据    |
| data.secret  | String  | 井通钱包私钥           |
| data.address | String  | 井通钱包地址           |


### 4.2 创建连接获取服务器基础信息

#### 类型 

GET 

#### 描述

创建连接获取服务器基础信息

#### 参数说明

无

#### 请求地址
```
{{host}}/swtclib/remote/server/info
```
#### cURL

```curl
curl --location --request GET "{{host}}/swtclib/remote/server/info"
```
#### 返回值示例

```JSON
{
    "success": true,
    "msg": "成功",
    "code": 0,
    "data": {
        "fee_base": 10,
        "fee_ref": 10,
        "hostid": "PET",
        "ledger_hash": "3C88EFDF8F051D7038CC871D0A2F6641853D4FE7161A8F7BD89BC28FC7E4C80C",
        "ledger_index": 14508242,
        "ledger_time": 628242750,
        "load_base": 256,
        "load_factor": 256,
        "pubkey_node": "n9M4oEaMGxjWsyMtp9sYAGgZbjoC4W7cETbTDJrUuUHv9KYU9ALb",
        "random": "6DC4208C2D8A7D37414ACE6274426142D98D086BB8719019748F35A7794CA97B",
        "reserve_base": 20000000,
        "reserve_inc": 5000000,
        "server_status": "full",
        "validated_ledgers": "266955-14508242"
    }
}
```
#### 返回值解析

| 参数                   | 类型    | 说明                         |
|------------------------|---------|----------------------------|
| success                | Boolean | 此次请求是否成功             |
| msg                    | String  | 返回的信息                   |
| code                   | Integer | 服务器返回的请求状态码       |
| data                   | Object  | SWTC-LIB 返回的数据          |
| data.fee_base          | Integer | 基础费用(手续费计算公式因子) |
| data.fee_ref           | Integer | 引用费用(手续费计算公式因子) |
| data.hostid            | String  | 主机名                       |
| data.ledger_hash       | String  | 账本 hash                    |
| data.ledger_index      | Integer | 区块高度                     |
| data.ledger_time       | Integer | 账本关闭时间                 |
| data.pubkey_node       | String  | 节点公钥                     |
| data.reserve_base      | Integer | 账号保留值                   |
| data.reserve_inc       | Integer | 用户每次挂单或信任冻结数量   |
| data.server_status     | String  | 服务器状态                   |
| data.validated_ledgers | String  | 账本区间                     |

### 4.4 请求底层服务器信息

#### 类型 

GET 

#### 描述

创建连接获取底层服务器信息

#### 参数说明

无

#### 请求地址
```
{{host}}/swtclib/remote/server/bottom
```
#### cURL

```curl
curl --location --request GET "{{host}}/swtclib/remote/server/bottom"
```
#### 返回值示例

```JSON
{
    "success": true,
    "msg": "成功",
    "code": 0,
    "data": {
        "complete_ledgers": "266955-14508246",
        "ledger": "EFD3F78EA25A23FE1521B04E5673D02081E7843A0EFFF20D04E5B7FC97E1DDB2",
        "public_key": "n9M4oEaMGxjWsyMtp9sYAGgZbjoC4W7cETbTDJrUuUHv9KYU9ALb",
        "state": "full   27:03:19",
        "peers": 35,
        "version": "skywelld-0.28.1"
    }
}
```
#### 返回值解析

| 参数         | 类型    | 说明                   |
|--------------|---------|----------------------|
| success      | Boolean | 此次请求是否成功       |
| msg          | String  | 返回的信息             |
| code         | Integer | 服务器返回的请求状态码 |
| data         | Object  | SWTC-LIB 返回的数据    |
| data.version | String  | 服务器部署项目版本     |
| data.ledgers | String  | 账本区间               |
| data.node    | String  | 节点公钥               |
| data.state   | String  | 服务器状态             |

### 4.5 获取最新账本信息

#### 类型 

GET 

#### 描述

获取最新账本信息

#### 参数说明

无

#### 请求地址
```
{{host}}/swtclib/remote/ledger/new
```
#### cURL

```curl
curl --location --request GET "{{host}}/swtclib/remote/ledger/new"
```
#### 返回值示例

```JSON
{
    "success": true,
    "msg": "成功",
    "code": 0,
    "data": {
        "ledger_hash": "18166576B066E5AE365DDAC2021414DDF79CA78835A10CF4776932762A4D5A6B",
        "ledger_index": 14508250
    }
}
```
#### 返回值解析

| 参数              | 类型    | 说明                   |
|-------------------|---------|----------------------|
| success           | Boolean | 此次请求是否成功       |
| msg               | String  | 返回的信息             |
| code              | Integer | 服务器返回的请求状态码 |
| data              | Object  | SWTC-LIB 返回的数据    |
| data.ledger_hash  | String  | 账本 hash              |
| data.ledger_index | String  | 账本高度/区块高度      |


### 4.6.1 根据hash获取某一账本具体信息

#### 类型 

GET 

#### 描述

获取某一账本具体信息

#### 请求地址
```
{{host}}/swtclib/remote/ledger/hash/:hash
```

#### 参数说明

##### 参数介绍

| 参数         | 类型     | 说明                                              |
|--------------|----------|-------------------------------------------------|
| hash         | String   | 井通区块 hash                                     |
| transactions | Boolean? | 可选参数,是否返回账本上的交易记录 hash，默认 false |

#### cURL

```curl
curl --location --request GET "{{host}}/swtclib/remote/ledger/hash/:hash?transactions=true"
```
#### 返回值示例

```JSON
{
    "success": true,
    "msg": "成功",
    "code": 0,
    "data": {
        "accepted": true,
        "account_hash": "C1EA1C0FAE091C8C48D2B5D845672DE427613A59286BD47C3E0540FC15FE88A5",
        "close_time": 628239630,
        "close_time_human": "2019-Nov-28 07:00:30",
        "close_time_resolution": 10,
        "closed": true,
        "hash": "4C235B8BC90B29B5AE314CB75EC192C57FA3721D9EABA94C1DCB589BDE98BCA1",
        "ledger_hash": "4C235B8BC90B29B5AE314CB75EC192C57FA3721D9EABA94C1DCB589BDE98BCA1",
        "ledger_index": "14507930",
        "parent_hash": "8D285D318F1BEF02F4321EED78BCD6A45D65E553F1CAA7423FB82CD42E6ED7AE",
        "seqNum": "14507930",
        "totalCoins": "599999999999460713",
        "total_coins": "599999999999460713",
        "transaction_hash": "73E29E4E204813D87E6E5DCD0A6EC9AADE563F96DDF2CEF19EE7DE5640E1EDCA",
        "transactions": [
            "0DF707C0E476994471A51E37C29A562A3F1DD6A297D378A8AF5DF0E649C17B9B",
            "1FE128ABDD8C72A9AF84648A081D1BAC74B6477C32C9EAD440544EDA5C364CF4",
            "31EA2542D36668383D7A21A6F1FB741C61D5BB5FBA655BB23BA8FE41E3BECFC9",
            "41E81C6F821AB8499FE4443F92BE9079AA561B05D14F20ED6F4BE9B92A53E68A",
            ......
        ]
    }
}
```
#### 返回值解析

| 参数                        | 类型    | 说明                   |
|-----------------------------|---------|----------------------|
| success                     | Boolean | 此次请求是否成功       |
| msg                         | String  | 返回的信息             |
| code                        | Integer | 服务器返回的请求状态码 |
| data                        | Object  | SWTC-LIB 返回的数据    |
| data.accepted               | Boolean | 区块是否已经产生       |
| data.account_hash           | String  | 状态 hash 树根         |
| data.close_time             | Integer | 关闭时间               |
| data.close_time_human       | String  | 关闭时间               |
| data.close_time_resoluti on | Integer | 关闭周期               |
| data.closed                 | Boolean | 账本是否已经关闭       |
| data.hash                   | String  | 账本 hash              |
| data.ledger_hash            | String  | 账本 hash              |
| data.ledger_index           | String  | 账本高度/区块高度      |
| data.parent_hash            | String  | 上一区块 hash 值       |
| data.seqNum                 | String  | 账本高度/区块高度      |
| data.totalCoins             | String  | swt 总量               |
| data.total_coins            | String  | swt 总量               |
| data.transaction_hash       | String  | 交易 hash 树根         |
| data.transactions           | Array   | 该账本里的交易列表     |
| data.transactions[0]        | String  | 交易Hash               |

### 4.6.2 根据账本高度获取某一账本具体信息

#### 类型 

GET 

#### 描述

获取某一账本具体信息

#### 请求地址
```
{{host}}/swtclib/remote/ledger/index/:index
```

#### 参数说明

##### 参数介绍

| 参数         | 类型     | 说明                                              |
|--------------|----------|-------------------------------------------------|
| index        | String   | 井通区块高度                                      |
| transactions | Boolean? | 可选参数,是否返回账本上的交易记录 hash，默认 false |

#### cURL

```curl
curl --location --request GET "{{host}}/swtclib/remote/ledger/index/:index?transactions=true"
```
#### 返回值示例

```JSON
{
    "success": true,
    "msg": "成功",
    "code": 0,
    "data": {
        "accepted": true,
        "account_hash": "C1EA1C0FAE091C8C48D2B5D845672DE427613A59286BD47C3E0540FC15FE88A5",
        "close_time": 628239630,
        "close_time_human": "2019-Nov-28 07:00:30",
        "close_time_resolution": 10,
        "closed": true,
        "hash": "4C235B8BC90B29B5AE314CB75EC192C57FA3721D9EABA94C1DCB589BDE98BCA1",
        "ledger_hash": "4C235B8BC90B29B5AE314CB75EC192C57FA3721D9EABA94C1DCB589BDE98BCA1",
        "ledger_index": "14507930",
        "parent_hash": "8D285D318F1BEF02F4321EED78BCD6A45D65E553F1CAA7423FB82CD42E6ED7AE",
        "seqNum": "14507930",
        "totalCoins": "599999999999460713",
        "total_coins": "599999999999460713",
        "transaction_hash": "73E29E4E204813D87E6E5DCD0A6EC9AADE563F96DDF2CEF19EE7DE5640E1EDCA",
        "transactions": [
            "0DF707C0E476994471A51E37C29A562A3F1DD6A297D378A8AF5DF0E649C17B9B",
            "1FE128ABDD8C72A9AF84648A081D1BAC74B6477C32C9EAD440544EDA5C364CF4",
            "31EA2542D36668383D7A21A6F1FB741C61D5BB5FBA655BB23BA8FE41E3BECFC9",
            "41E81C6F821AB8499FE4443F92BE9079AA561B05D14F20ED6F4BE9B92A53E68A",
            ......
        ]
    }
}
```
#### 返回值解析

| 参数                        | 类型    | 说明                   |
|-----------------------------|---------|----------------------|
| success                     | Boolean | 此次请求是否成功       |
| msg                         | String  | 返回的信息             |
| code                        | Integer | 服务器返回的请求状态码 |
| data                        | Object  | SWTC-LIB 返回的数据    |
| data.accepted               | Boolean | 区块是否已经产生       |
| data.account_hash           | String  | 状态 hash 树根         |
| data.close_time             | Integer | 关闭时间               |
| data.close_time_human       | String  | 关闭时间               |
| data.close_time_resoluti on | Integer | 关闭周期               |
| data.closed                 | Boolean | 账本是否已经关闭       |
| data.hash                   | String  | 账本 hash              |
| data.ledger_hash            | String  | 账本 hash              |
| data.ledger_index           | String  | 账本高度/区块高度      |
| data.parent_hash            | String  | 上一区块 hash 值       |
| data.seqNum                 | String  | 账本高度/区块高度      |
| data.totalCoins             | String  | swt 总量               |
| data.total_coins            | String  | swt 总量               |
| data.transaction_hash       | String  | 交易 hash 树根         |
| data.transactions           | Array   | 该账本里的交易列表     |
| data.transactions[0]        | String  | 交易Hash               |


### 4.7 查询某一交易具体信息

#### 类型 

GET 

#### 描述

查询某一交易具体信息


#### 请求地址
```
{{host}}/swtclib/remote/tx/:hash
```

#### 参数说明

##### 参数介绍

| 参数 | 类型   | 说明      |
|------|--------|---------|
| hash | String | 交易 hash |


#### cURL

```curl
curl --location --request GET "{{host}}/swtclib/remote/tx/:hash"
```
#### 返回值示例

```JSON
{
    "success": true,
    "msg": "成功",
    "code": 0,
    "data": {
        "Account": "jJCtKD2MbfYoVdQEbjTmbXmNiVkLBTknLC",
        "Amount": {
            "currency": "TEST",
            "issuer": "jGa9J9TkqtBcUoHe2zqhVFFbgUVED6o9or",
            "value": "0.01"
        },
        "Destination": "jpv789PmsKzWbhWVNer1ZAkzuXW7kLCBKs",
        "Fee": "10000",
        "Flags": 0,
        "Memos": [
            {
                "Memo": {
                    "MemoData": "E6B58BE8AF9531"
                }
            }
        ],
        "Sequence": 4112,
        "SigningPubKey": "0256F9ED0A13D879E2DAC205A23CF1BA6DA210C094F3B18168945BBCD0664BAD0C",
        "TransactionType": "Payment",
        "TxnSignature": "3045022100938436B572BC335EB8F0A5D01F11A196E3F0EAEF9C30511D022DF207BC0451C402207D4BD259B3EC104420FB6BAC1DBA1BBB67049AEB9A89B719A24C33FB959E3FA7",
        "date": 628224400,
        "hash": "92AFDB9F02F7CF913EB1F32E076346BF48AA317F64BD3D203E156622E57741E2",
        "inLedger": 14506407,
        "ledger_index": 14506407,
        "meta": {
            "AffectedNodes": [
                {
                    "ModifiedNode": {
                        "FinalFields": {
                            "Account": "jJCtKD2MbfYoVdQEbjTmbXmNiVkLBTknLC",
                            "Balance": "760339232",
                            "Flags": 0,
                            "OwnerCount": 8,
                            "Sequence": 4113
                        },
                        "LedgerEntryType": "AccountRoot",
                        "LedgerIndex": "AE6D3CDFAE02DB31C48C784932FEE86709D554F1FB5E86D7636A2858D396130E",
                        "PreviousFields": {
                            "Balance": "760349232",
                            "Sequence": 4112
                        },
                        "PreviousTxnID": "FF815CCC3B685C3807DFDEAB21CAF288AE59705D9EEAD75136212601D232AAC2",
                        "PreviousTxnLgrSeq": 14506302
                    }
                }
            ],
            "TransactionIndex": 2,
            "TransactionResult": "tecNO_DST"
        },
        "validated": true
    }
}
```
#### 返回值解析

| 参数                        | 类型           | 说明                   |
|-----------------------------|----------------|------------------------|
| success                     | Boolean        | 此次请求是否成功       |
| msg                         | String         | 返回的信息             |
| code                        | Integer        | 服务器返回的请求状态码 |
| data                        | Object         | SWTC-LIB 返回的数据    |
| data.Account                | String         | 钱包地址               |
| data.Amount                 | String/O bject | 交易金额               |
| data.Destination            | String         | 交易对家地址           |
| data.Fee                    | String         | 交易费                 |
| data.Flags                  | Integer        | 交易标记               |
| data.Memos                  | Array          | 备注                   |
| data.Sequence               | Integer        | 自身账号的交易号       |
| data.SigningPubKey          | String         | 签名公钥               |
| data.Timestamp              | Integer        | 交易提交时间戳         |
| data.TransactionType        | String         | 交易类型               |
| data.TxnSignature           | String         | 交易签名               |
| data.date                   | Integer        | 交易进账本时间         |
| data.hash                   | String         | 交易 hash              |
| data.inLedger               | Integer        | 交易所在的账本号       |
| data.ledger_index           | Integer        | 账本高度               |
| data.meta                   | Object         | 交易影响的节点         |
| data.meta.AffectedNodes     | Array          | 受影响的节点           |
| data.meta.TransactionIndex  | Integer        | --                     |
| data.meta.TransactionResult | String         | 交易结果               |
| data.validated              | Boolean        | 交易是否通过验证       |

### 4.8.1 请求账号信息

#### 类型 

GET 

#### 描述

请求账号信息


#### 请求地址
```
{{host}}/swtclib/remote/account/:account
```

#### 参数说明

##### 参数介绍

| 参数    | 类型   | 说明         |
|---------|--------|------------|
| account | String | 井通钱包地址 |


#### cURL

```curl
curl --location --request GET "{{host}}/swtclib/remote/account/:account"
```
#### 返回值示例

```JSON
{
    "success": true,
    "msg": "成功",
    "code": 0,
    "data": {
        "account_data": {
            "Account": "jJCtKD2MbfYoVdQEbjTmbXmNiVkLBTknLC",
            "Balance": "760169232",
            "Flags": 0,
            "LedgerEntryType": "AccountRoot",
            "OwnerCount": 8,
            "PreviousTxnID": "A749406C4510BF857548B463D6C11D337B64AF9D564EA5E30C6FAF170D77FEC3",
            "PreviousTxnLgrSeq": 14507953,
            "Sequence": 4129,
            "index": "AE6D3CDFAE02DB31C48C784932FEE86709D554F1FB5E86D7636A2858D396130E"
        },
        "ledger_hash": "5339FFB91BA077BF6E0B198EAD7D6DD410C14906D47AE5CFA11A9F2D45C3361A",
        "ledger_index": 14508309,
        "validated": true
    }
}
```
#### 返回值解析

| 参数                                | 类型    | 说明                                  |
|-------------------------------------|---------|---------------------------------------|
| success                             | Boolean | 此次请求是否成功                      |
| msg                                 | String  | 返回的信息                            |
| code                                | Integer | 服务器返回的请求状态码                |
| data                                | Object  | SWTC-LIB 返回的数据                   |
| data.account_data                   | Object  | 账号信息                              |
| data.account_data.Account           | String  | 钱包地址                              |
| data.account_data.Balance           | String  | swt 数量                              |
| data.account_data.Domain            | String  | 域名                                  |
| data.account_data.Flags             | Integer | 属性标志                              |
| data.account_data.MessageKey        | String  | 公共密钥，用于发送加密的邮件到这个帐户 |
| data.account_data.OwnerCount        | Integer | 用户拥有的挂单数和信任线数量的总和    |
| data.account_data.PreviousTxnID     | String  | 操作该帐号的上一笔交易 hash           |
| data.account_data.PreviousTxnLgrSeq | Integer | 该帐号上一笔交易所在的账本号          |
| data.account_data.RegularKey        | String  | RegularKey                            |
| data.account_data.Sequence          | Integer | 账号当前序列号                        |
| data.account_data.TransferRate      | Integer | 手续费汇率                            |
| data.account_data.index             | String  | 该数据所在索引 hash                   |
| data.ledger_hash                    | String  | 账本 hash                             |
| data.ledger_index                   | Integer | 账本高度                              |
| data.validated                      | Boolean | 交易是否通过验证                      |

### 4.8.2 请求余额

#### 类型 

GET 

#### 描述

请求账号信息


#### 请求地址
```
{{host}}/swtclib/remote/balance/:account
```

#### 参数说明

##### 参数介绍

| 参数     | 类型    | 说明             |
|----------|---------|----------------|
| account  | String  | 井通钱包地址     |
| currency | String? | 特定的币种       |
| issuer   | String? | 特定币种的发行商 |


#### cURL

```curl
curl --location --request GET "{{host}}/swtclib/remote/balance/:account?currency=CSP&issuer=jGa9J9TkqtBcUoHe2zqhVFFbgUVED6o9or"
```
#### 返回值示例

```JSON
{
    "success": true,
    "msg": "成功",
    "code": 0,
    "data": {
        "balances": [
            {
                "value": "760.169232",
                "currency": "SWT",
                "issuer": "",
                "freezed": "60.000000"
            },
            {
                "value": "97.000000",
                "currency": "TFG",
                "issuer": "jGa9J9TkqtBcUoHe2zqhVFFbgUVED6o9or",
                "freezed": "0.000000"
            },
            {
                "value": "11.000000",
                "currency": "JSLASH",
                "issuer": "jGa9J9TkqtBcUoHe2zqhVFFbgUVED6o9or",
                "freezed": "0.000000"
            },
            ......
        ],
        "sequence": 4129
    }
}
```
#### 返回值解析

| 参数                      | 类型    | 说明                   |
|---------------------------|---------|----------------------|
| success                   | Boolean | 此次请求是否成功       |
| msg                       | String  | 返回的信息             |
| code                      | Integer | 服务器返回的请求状态码 |
| data                      | Object  | SWTC-LIB 返回的数据    |
| data.balances             | Array   | 余额信息的数组         |
| data.balances[0].value    | String  | 余额，小数点后六位      |
| data.balances[0].currency | String  | 币种                   |
| data.balances[0].issuer   | String  | 发行商                 |
| data.balances[0].freezed  | String  | 冻结数，小数点后六位    |

### 4.12 获得账号交易列表

#### 类型 

GET 

#### 描述

获得账号交易列表


#### 请求地址
```
{{host}}/swtclib/remote/tx/list/:account
```

#### 参数说明

##### 参数介绍

| 参数          | 类型    | 说明                                                       |
|---------------|---------|----------------------------------------------------------|
| account       | String  | 井通钱包地址                                               |
| limit         | String? | 查询多少条(默认20,最大值200)                               |
| forward       | String? | 按交易时间排序，固定的两个值：asc(升序)、desc(降序)(默认desc) |
| marker_ledger | String? | 上一个查询的marker.ledger这里起到分页的作用                |
| marker_seq    | String? | 上一个查询的marker.seq这里起到分页的作用                   |


#### cURL

```curl
curl --location --request GET "{{host}}/swtclib/remote/tx/list/:account?limit=10&forward=asc&marker_ledger=14264080&marker_seq=0"
```
#### 返回值示例

```JSON
{
    "success": true,
    "msg": "获取交易列表成功",
    "code": 0,
    "data": {
        "account": "jJCtKD2MbfYoVdQEbjTmbXmNiVkLBTknLC",
        "ledger_index_max": 14508365,
        "ledger_index_min": 266955,
        "limit": 1,
        "marker": {
            "ledger": 14264153,
            "seq": 8
        },
        "transactions": [
            {
                "date": 1572485910,
                "hash": "3B0B6C9E5FAB5172F67C2E431D286DED6123418DEF5050EC7BD95337AB80CEED",
                "type": "received",
                "fee": "0.01",
                "result": "tesSUCCESS",
                "memos": [
                    {
                        "MemoData": "remark=测试"
                    }
                ],
                "counterparty": "jLamHt9mBcoiaAjf5huKuX5iFnrNPfBpWV",
                "amount": {
                    "currency": "TFG",
                    "issuer": "jGa9J9TkqtBcUoHe2zqhVFFbgUVED6o9or",
                    "value": "100"
                },
                "effects": [],
                "balances": {
                    "TFG": 100
                },
                "balancesPrev": {
                    "TFG": 0
                }
            }
        ]
    }
}
```
#### 返回值解析

| 参数                                 | 类型    | 说明                         |
|--------------------------------------|---------|----------------------------|
| success                              | Boolean | 此次请求是否成功             |
| msg                                  | String  | 返回的信息                   |
| code                                 | Integer | 服务器返回的请求状态码       |
| data                                 | Object  | SWTC-LIB 返回的数据          |
| data.account                         | String  | 钱包地址                     |
| data.ledger_index_max                | Integer | 当前节点缓存的账本区间最大值 |
| data.ledger_index_min                | Integer | 当前节点缓存的账本区间最小值 |
| data.marker                          | Object  | 查到的当前记录标记           |
| data.transactions                    | Array   | 交易记录列表                 |
| data.transactions[0].date            | Integer | 时间戳                       |
| data.transactions[0].hash            | String  | 交易hash                     |
| data.transactions[0].type            | String  | 交易类型                     |
| data.transactions[0].fee             | String  | 手续费                       |
| data.transactions[0].result          | String  | 交易结果                     |
| data.transactions[0].memos           | Array   | 备注                         |
| data.transactions[0].counterparty    | String  | 交易对家                     |
| data.transactions[0].amount          | Object  | 交易金额对象                 |
| data.transactions[0].amount.value    | String  | 金额                         |
| data.transactions[0].amount.currency | String  | 货币种类                     |
| data.transactions[0].amount.issuer   | String  | 货币                         |
| data.transactions[0].effects         | Array   | 交易效果                     |


### 4.15.1 单笔支付

#### 类型 

POST 

#### 描述

单笔支付


#### 请求地址
```
{{host}}/swtclib/remote/tx
```

#### 参数说明

##### 参数介绍

| 参数     | 类型    | 说明                                        |
|----------|---------|-------------------------------------------|
| account  | String  | 发起账号                                    |
| to       | String  | 目标账号                                    |
| value    | String  | 支付数量                                    |
| currency | String  | 货币种类，三到六个字母或 20 字节的自定义货币 |
| issuer   | String  | 货币发行方，无则留 ''                        |
| secret   | String  | 井通钱包私钥                                |
| addMemo  | String? | 备注信息                                    |

##### 参数示例

```JSON
{
  "account":"jJCtKD2MbfYoVdQEbjTmbXmNiVkLBTknLC",
  "to":"jfAUjEen8cLvRmCGyZYYwumLEZG45PThiR",
  "value":"0.01",
  "currency":"SWT",
  "issuer":"jGa9J9TkqtBcUoHe2zqhVFFbgUVED6o9or",
  "secret":"snXXXXXXXXXXXXXXXXXXXXXXXXXXX",
  "addMemo":"测试"
}
```

#### cURL

```curl
curl --location --request POST "{{host}}/swtclib/remote/tx" \
--header "Content-Type: application/json" \
--data "{
  \"account\":\"jJCtKD2MbfYoVdQEbjTmbXmNiVkLBTknLC\",
  \"to\":\"jfAUjEen8cLvRmCGyZYYwumLEZG45PThiR\",
  \"value\":\"0.01\",
  \"currency\":\"SWT\",
  \"issuer\":\"jGa9J9TkqtBcUoHe2zqhVFFbgUVED6o9or\",
  \"secret\":\"snXXXXXXXXXXXXXXXXXXXXXXXXXXX\",
  \"addMemo\":\"测试\"
}"
```
#### 返回值示例

```JSON
{
    "success": true,
    "msg": "成功",
    "code": 0,
    "data": {
        "engine_result": "tesSUCCESS",
        "engine_result_code": 0,
        "engine_result_message": "The transaction was applied. Only final in a validated ledger.",
        "tx_blob": "120000220000000024000000126140000000000F4240684000000000002710732103FF13DC19ABEBA0AB17A4BCE6931F8487405BB41C60605DD839C4F22B0BBBE79974463044022061B5D8672CA00FA671648828A189562AEB1FE05610E869D53DB3B6CB5CBED94702204B141328BF03DD2A9D43AF957D1828A821D8BD384D650E35C56AF5605EFB0761811459A0172E3454FA1FA7FEED20E498308152C1FF6883140D2C803B102F69C7AF902747C0CE6B0C90CF869AF9EA7D0CE6B58BE8AF95E8BDACE8B4A6E1F1",
        "tx_json": {
            "Account": "j9wtvMqV3jYpjHcHS94yXW8XGNB7YHC8w8",
            "Amount": "1000000",
            "Destination": "jpUCa7JwSbwvU1adNXRN7BWzTeVsTiNp1i",
            "Fee": "10000",
            "Flags": 0,
            "Memos": [
                {
                    "Memo": {
                        "MemoData": "E6B58BE8AF95E8BDACE8B4A6"
                    }
                }
            ],
            "Sequence": 18,
            "SigningPubKey": "03FF13DC19ABEBA0AB17A4BCE6931F8487405BB41C60605DD839C4F22B0BBBE799",
            "TransactionType": "Payment",
            "TxnSignature": "3044022061B5D8672CA00FA671648828A189562AEB1FE05610E869D53DB3B6CB5CBED94702204B141328BF03DD2A9D43AF957D1828A821D8BD384D650E35C56AF5605EFB0761",
            "hash": "B69BA8AE7CA50D17FA71CBA328E7CD9576349E296AF918073F905475D89C5ABC"
        }
    }
}
```
#### 返回值解析

| 参数                         | 类型    | 说明                   |
|------------------------------|---------|----------------------|
| success                      | Boolean | 此次请求是否成功       |
| msg                          | String  | 返回的信息             |
| code                         | Integer | 服务器返回的请求状态码 |
| data                         | Object  | SWTC-LIB 返回的数据    |
| data.engine_result           | String  | 请求结果               |
| data.engine_result_code      | Array   | 请求结果编码           |
| data.engine_result_message   | String  | 请求结果 message 信息  |
| data.tx_blob                 | String  | 16 进制签名后的交易    |
| data.tx_json                 | Object  | 交易内容               |
| data.tx_json.Account         | String  | 账号地址               |
| data.tx_json.Amount          | String  | 交易金额               |
| data.tx_json.Destination     | String  | 对家                   |
| data.tx_json.Fee             | String  | 交易费                 |
| data.tx_json.Flags           | Integer | 交易标记               |
| data.tx_json.Memos           | Array   | 备注                   |
| data.tx_json.Sequence        | Integer | 单子序列号             |
| data.tx_json.SigningPubKey   | Object  | 签名公钥               |
| data.tx_json.TransactionType | String  | 交易类型               |
| data.tx_json.TxnSignature    | String  | 交易签名               |
| data.tx_json.hash            | String  | 交易 hash              |

### 4.15.2 需要sequence的串行批量支付

#### 类型 

POST 

#### 描述

需要sequence的串行批量支付


#### 请求地址
```
{{host}}/swtclib/remote/tx/serial
```

#### 参数说明

* server、serverIssuer、sequence都是可选参数。
* 若不填写server和serverIssuer，服务器会根据配置中的单台服务器进行sequence进行交易。
* sequence若不填写，则服务器会进行默认的单笔交易，若填写，服务器会进行带上sequence的交易

##### 参数介绍

| 参数         | 类型    | 说明                                        |
|--------------|---------|-------------------------------------------|
| server       | String? | 指定的连接单台服务器节点的地址              |
| serverIssuer | String? | 指定的连接单台服务器节点的发行商            |
| sequence     | String? | 发起账号的sequence                          |
| account      | String  | 发起账号                                    |
| to           | String  | 目标账号                                    |
| value        | String  | 支付数量                                    |
| currency     | String  | 货币种类，三到六个字母或 20 字节的自定义货币 |
| issuer       | String  | 货币发行方，无则留 ''                        |
| secret       | String  | 井通钱包私钥                                |
| addMemo      | String? | 备注信息                                    |

##### 参数示例

```JSON
{
  "server":"ws://106.54.116.47:5020",
  "serverIssuer":"jBciDE8Q3uJjf111VeiUNM775AMKHEbBLS",
  "sequence":"4122",
  "account":"jJCtKD2MbfYoVdQEbjTmbXmNiVkLBTknLC",
  "secret":"snXXXXXXXXXXXXXXXXXXXXXXXXXXX",
  "to":"jpUCa7JwSbwvU1adNXRN7BWzTeVsTiNp1i",
  "value":"0.01",
  "currency":"TEST",
  "issuer":"jGa9J9TkqtBcUoHe2zqhVFFbgUVED6o9or",
  "addMemo":"测试"
}
```

#### cURL

```curl
curl --location --request POST "{{host}}/swtclib/remote/tx/serial" \
--header "Content-Type: application/json" \
--data "{
  \"server\":\"ws://106.54.116.47:5020\",
  \"serverIssuer\":\"jBciDE8Q3uJjf111VeiUNM775AMKHEbBLS\",
  \"sequence\":\"4122\",
  \"account\":\"jJCtKD2MbfYoVdQEbjTmbXmNiVkLBTknLC\",
  \"secret\":\"snXXXXXXXXXXXXXXXXXXXXXXXXXXX\",
  \"to\":\"jpUCa7JwSbwvU1adNXRN7BWzTeVsTiNp1i\",
  \"value\":\"0.01\",
  \"currency\":\"TEST\",
  \"issuer\":\"jGa9J9TkqtBcUoHe2zqhVFFbgUVED6o9or\",
  \"addMemo\":\"测试\"
}"
```
#### 返回值示例

```JSON
{
    "success": true,
    "msg": "请求成功",
    "code": 0,
    "data": {
        "engine_result": "tesSUCCESS",
        "engine_result_code": 0,
        "engine_result_message": "The transaction was applied. Only final in a validated ledger.",
        "tx_blob": "1200002200000000240000102161D4038D7EA4C680000000000000000000000000544553540000000000A582E432BFC48EEDEF852C814EC57F3CD2D4159668400000000000271073210256F9ED0A13D879E2DAC205A23CF1BA6DA210C094F3B18168945BBCD0664BAD0C74473045022100C082DAB4DB4534908F21B2D20EA31086A2C8D7159C614E88D83DADD5461BB49D0220106CFD6AD424AA64248C9B95945F2BC6A2119C20C7076158CB5579C4B6F6F6FE8114C1D4C79B2C9CD8FE9AB1EE29FAA18432A3DBFD8A83140D2C803B102F69C7AF902747C0CE6B0C90CF869AF9EA7D06E6B58BE8AF95E1F1",
        "tx_json": {
            "Account": "jJCtKD2MbfYoVdQEbjTmbXmNiVkLBTknLC",
            "Amount": {
                "currency": "TEST",
                "issuer": "jGa9J9TkqtBcUoHe2zqhVFFbgUVED6o9or",
                "value": "0.01"
            },
            "Destination": "jpUCa7JwSbwvU1adNXRN7BWzTeVsTiNp1i",
            "Fee": "10000",
            "Flags": 0,
            "Memos": [
                {
                    "Memo": {
                        "MemoData": "E6B58BE8AF95"
                    }
                }
            ],
            "Sequence": 4129,
            "SigningPubKey": "0256F9ED0A13D879E2DAC205A23CF1BA6DA210C094F3B18168945BBCD0664BAD0C",
            "TransactionType": "Payment",
            "TxnSignature": "3045022100C082DAB4DB4534908F21B2D20EA31086A2C8D7159C614E88D83DADD5461BB49D0220106CFD6AD424AA64248C9B95945F2BC6A2119C20C7076158CB5579C4B6F6F6FE",
            "hash": "AAACDEB43EC8B70EDF84201F2BA60293A22064F94F8DB9630539538092101E4F"
        }
    }
}
```
#### 返回值解析

| 参数                         | 类型    | 说明                   |
|------------------------------|---------|----------------------|
| success                      | Boolean | 此次请求是否成功       |
| msg                          | String  | 返回的信息             |
| code                         | Integer | 服务器返回的请求状态码 |
| data                         | Object  | SWTC-LIB 返回的数据    |
| data.engine_result           | String  | 请求结果               |
| data.engine_result_code      | Array   | 请求结果编码           |
| data.engine_result_message   | String  | 请求结果 message 信息  |
| data.tx_blob                 | String  | 16 进制签名后的交易    |
| data.tx_json                 | Object  | 交易内容               |
| data.tx_json.Account         | String  | 账号地址               |
| data.tx_json.Amount          | String  | 交易金额               |
| data.tx_json.Destination     | String  | 对家                   |
| data.tx_json.Fee             | String  | 交易费                 |
| data.tx_json.Flags           | Integer | 交易标记               |
| data.tx_json.Memos           | Array   | 备注                   |
| data.tx_json.Sequence        | Integer | 单子序列号             |
| data.tx_json.SigningPubKey   | Object  | 签名公钥               |
| data.tx_json.TransactionType | String  | 交易类型               |
| data.tx_json.TxnSignature    | String  | 交易签名               |
| data.tx_json.hash            | String  | 交易 hash              |

### 4.15.3 不需要sequence的串行批量支付

#### 类型 

POST 

#### 描述

不需要sequence的串行批量支付


#### 请求地址
```
{{host}}/swtclib/remote/tx/limit
```

#### 参数说明

##### 参数介绍

| 参数           | 类型    | 说明                                        |
|----------------|---------|-------------------------------------------|
| account        | String  | 发起账号                                    |
| secret         | String  | 井通钱包私钥                                |
| tx             | Array   | 需要交易的地址对                            |
| tx[0].to       | String  | 目标账号                                    |
| tx[0].value    | String  | 支付数量                                    |
| tx[0].currency | String  | 货币种类，三到六个字母或 20 字节的自定义货币 |
| tx[0].issuer   | String  | 货币发行方，无则留 ''                        |
| tx[0].addMemo  | String? | 备注信息                                    |

##### 参数示例

```JSON
{
  "account":"jJCtKD2MbfYoVdQEbjTmbXmNiVkLBTknLC",
  "secret":"snXXXXXXXXXXXXXXXXXXXXXXXXXXX",
  "tx":[
    {
      "to":"jpUCa7JwSbwvU1adNXRN7BWzTeVsTiNp1i",
      "value":"0.01",
      "currency":"TEST",
      "issuer":"jGa9J9TkqtBcUoHe2zqhVFFbgUVED6o9or",
      "addMemo":"测试1"
    },
    {
      "to":"jpUCa7JwSbwvU1adNXRN7BWzTeVsTiNp1i",
      "value":"0.01",
      "currency":"TEST",
      "issuer":"jGa9J9TkqtBcUoHe2zqhVFFbgUVED6o9or",
      "addMemo":"测试2"
    },
    {
      "to":"jpUCa7JwSbwvU1adNXRN7BWzTeVsTiNp1i",
      "value":"0.01",
      "currency":"TEST",
      "issuer":"jGa9J9TkqtBcUoHe2zqhVFFbgUVED6o9or",
      "addMemo":"测试2"
    }
  ]
}
```

#### cURL

```curl
curl --location --request POST "{{host}}/swtclib/remote/tx/limit" \
--header "Content-Type: application/json" \
--data "{
  \"account\":\"jJCtKD2MbfYoVdQEbjTmbXmNiVkLBTknLC\",
  \"secret\":\"snXXXXXXXXXXXXXXXXXXXXXXXXXXX\",
  \"tx\":[
    {
      \"to\":\"jpUCa7JwSbwvU1adNXRN7BWzTeVsTiNp1i\",
      \"value\":\"0.01\",
      \"currency\":\"TEST\",
      \"issuer\":\"jGa9J9TkqtBcUoHe2zqhVFFbgUVED6o9or\",
      \"addMemo\":\"测试1\"
    },
    {
      \"to\":\"jpUCa7JwSbwvU1adNXRN7BWzTeVsTiNp1i\",
      \"value\":\"0.01\",
      \"currency\":\"TEST\",
      \"issuer\":\"jGa9J9TkqtBcUoHe2zqhVFFbgUVED6o9or\",
      \"addMemo\":\"测试2\"
    },
    {
      \"to\":\"jpUCa7JwSbwvU1adNXRN7BWzTeVsTiNp1i\",
      \"value\":\"0.01\",
      \"currency\":\"TEST\",
      \"issuer\":\"jGa9J9TkqtBcUoHe2zqhVFFbgUVED6o9or\",
      \"addMemo\":\"测试2\"
    }
  ]
}"
```
#### 返回值示例

```JSON
{
    "success": true,
    "msg": "请求成功",
    "code": 0,
    "data": [
        {
            "success": true,
            "msg": "连接成功,交易结果为tesSUCCESS",
            "index": "0",
            "data": {
                "engine_result": "tesSUCCESS",
                "engine_result_code": 0,
                "engine_result_message": "The transaction was applied. Only final in a validated ledger.",
                "sequence": 4130,
                "hash": "231E38E970CBA2813D56658433EA6691E2056414D1EF00CB9E3E467C99AD6651"
            }
        },
        {
            "success": true,
            "msg": "连接成功,交易结果为tesSUCCESS",
            "index": "1",
            "data": {
                "engine_result": "tesSUCCESS",
                "engine_result_code": 0,
                "engine_result_message": "The transaction was applied. Only final in a validated ledger.",
                "sequence": 4131,
                "hash": "51B60B482D2927FAD6E5A70F07208E955D14003EFFB192E4E17B2413ECA1A870"
            }
        },
        {
            "success": true,
            "msg": "连接成功,交易结果为tesSUCCESS",
            "index": "2",
            "data": {
                "engine_result": "tesSUCCESS",
                "engine_result_code": 0,
                "engine_result_message": "The transaction was applied. Only final in a validated ledger.",
                "sequence": 4132,
                "hash": "82C82F9EBA37A7D836B8681562A2D2B6281AD04C8BE130D32FA6F8F5337584BF"
            }
        }
    ]
}
```

#### 返回值解析

| 参数                               | 类型    | 说明                                   |
|------------------------------------|---------|--------------------------------------|
| success                            | Boolean | 此次请求是否成功                       |
| msg                                | String  | 返回的信息                             |
| code                               | Integer | 服务器返回的请求状态码                 |
| data                               | Array   | 每一笔交易返回的数据                   |
| data[0].success                    | String  | 这一笔交易在提交到公共节点上是否有错误 |
| data[0].msg                        | String  | 这一笔交易在提交到公共节点上的提示信息 |
| data[0].index                      | String  | 每一笔在整个交易数组中的底标           |
| data[0].data                       | Array   | SWTC-LIB 返回的精简数据                |
| data[0].data.engine_result         | String  | 请求结果，根据是否为tesSUCCESS判断成功  |
| data[0].data.engine_result_code    | Integer | 请求结果编码                           |
| data[0].data.engine_result_message | String  | 请求结果 message 信息                  |
| data[0].data.Sequence              | Integer | 单子序列号                             |
| data[0].data.hash                  | String  | 交易 hash                              |


### 4.25 监听事件

目前支持两个监听事件:
- 监听所有交易(transactions)
- 监听所有账本(ledger_closed)

监听结果为标准的websock返回信息。

#### 使用说明

使用的是标准WS链接，测试地址为 ws://39.108.227.152:7900

监听如下两个事件：
- transactions
- ledger_closed

#### 代码示例

```JavaScript
<script src="./dist/socket.io.js"></script>
  <script>
    let serverHost = 'ws://127.0.0.1:7001';
    serverHost = 'ws://127.0.0.1:7900';
    var socket = io(serverHost);
    socket.on('connect', function(data){
      console.log(`connect->${serverHost}。获取到的socketId->${socket.id}`);
      console.log('开始接收交易和账本信息，如下所示(只打印hash)：');
    });
    socket.on('transactions', function(data){
      // console.log('transactions',data);
      console.log('transactions',data.transaction.hash);
    });
    socket.on('ledger_closed', function(data){
      // console.log('ledger_closed',data);
      console.log('ledger_closed',data.ledger_hash);
    });
    socket.on('disconnect', function(data){
      console.log('disconnect',data);
    });
  </script>
```
#### 可执行代码样例Exampl

代码样例在工程目录，example文件夹下面

#### 返回值

返回值根据SWTC-LIB，原封返回

## 附录

### 附录1:返回值Code说明

| code   | 说明               |
|--------|------------------|
| 0      | 正常返回,成功      |
| 400xxx | 参数错误           |
| 400000 | 参数不符合规范     |
| 401xxx | 需要身份验证       |
| 403xxx | 访问被拒绝         |
| 404xxx | 未找到资源         |
| 500xxx | 服务器出错         |
| 500000 | 服务器内部错误     |
| 503xxx | 服务器维护或者宕机 |