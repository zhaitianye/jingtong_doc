# swtclib_app

> 作为swtc-lib处理的中间层,提供 RESTFul API 接口服务

## 目录

<!-- TOC -->

- [swtclib_app](#swtclib_app)
  - [目录](#目录)
  - [接口文档](#接口文档)
    - [说明](#说明)
  - [服务器相关](#服务器相关)
    - [1.1 创建连接获取服务器基础信息](#11-创建连接获取服务器基础信息)
      - [类型](#类型)
      - [描述](#描述)
      - [参数说明](#参数说明)
      - [请求地址](#请求地址)
      - [cURL](#curl)
      - [返回值示例](#返回值示例)
      - [返回值解析](#返回值解析)
    - [1.2 请求底层服务器信息](#12-请求底层服务器信息)
      - [类型](#类型-1)
      - [描述](#描述-1)
      - [参数说明](#参数说明-1)
      - [请求地址](#请求地址-1)
      - [cURL](#curl-1)
      - [返回值示例](#返回值示例-1)
      - [返回值解析](#返回值解析-1)
  - [钱包相关](#钱包相关)
    - [2.1 创建钱包](#21-创建钱包)
      - [类型](#类型-2)
      - [描述](#描述-2)
      - [参数说明](#参数说明-2)
      - [请求地址](#请求地址-2)
      - [cURL](#curl-2)
      - [返回值示例](#返回值示例-2)
      - [返回值解析](#返回值解析-2)
    - [2.2 根据私钥创建钱包](#22-根据私钥创建钱包)
      - [类型](#类型-3)
      - [描述](#描述-3)
      - [参数说明](#参数说明-3)
        - [参数介绍](#参数介绍)
        - [参数示例](#参数示例)
      - [请求地址](#请求地址-3)
      - [cURL](#curl-3)
      - [返回值示例](#返回值示例-3)
      - [返回值解析](#返回值解析-3)
  - [账号相关](#账号相关)
    - [3.1 请求账号信息](#31-请求账号信息)
      - [类型](#类型-4)
      - [描述](#描述-4)
      - [请求地址](#请求地址-4)
      - [参数说明](#参数说明-4)
        - [参数介绍](#参数介绍-1)
      - [cURL](#curl-4)
      - [返回值示例](#返回值示例-4)
      - [返回值解析](#返回值解析-4)
    - [3.2 请求账号余额信息](#32-请求账号余额信息)
      - [类型](#类型-5)
      - [描述](#描述-5)
      - [请求地址](#请求地址-5)
      - [参数说明](#参数说明-5)
        - [参数介绍](#参数介绍-2)
      - [cURL](#curl-5)
      - [返回值示例](#返回值示例-5)
      - [返回值解析](#返回值解析-5)
    - [3.3 获得账号交易列表](#33-获得账号交易列表)
      - [类型](#类型-6)
      - [描述](#描述-6)
      - [请求地址](#请求地址-6)
      - [参数说明](#参数说明-6)
        - [参数介绍](#参数介绍-3)
      - [cURL](#curl-6)
      - [返回值示例](#返回值示例-6)
      - [返回值解析](#返回值解析-6)
  - [账本相关](#账本相关)
    - [4.1 获取最新关闭的账本信息](#41-获取最新关闭的账本信息)
      - [类型](#类型-7)
      - [描述](#描述-7)
      - [参数说明](#参数说明-7)
      - [请求地址](#请求地址-7)
      - [cURL](#curl-7)
      - [返回值示例](#返回值示例-7)
      - [返回值解析](#返回值解析-7)
    - [4.2 根据hash获取某一账本具体信息](#42-根据hash获取某一账本具体信息)
      - [类型](#类型-8)
      - [描述](#描述-8)
      - [请求地址](#请求地址-8)
      - [参数说明](#参数说明-8)
        - [参数介绍](#参数介绍-4)
      - [cURL](#curl-8)
      - [返回值示例](#返回值示例-8)
      - [返回值解析](#返回值解析-8)
    - [4.3 获取某一账本具体信息根据账本高度](#43-获取某一账本具体信息根据账本高度)
      - [类型](#类型-9)
      - [描述](#描述-9)
      - [请求地址](#请求地址-9)
      - [参数说明](#参数说明-9)
        - [参数介绍](#参数介绍-5)
      - [cURL](#curl-9)
      - [返回值示例](#返回值示例-9)
      - [返回值解析](#返回值解析-9)
  - [交易事务相关](#交易事务相关)
    - [5.1 查询某一交易具体信息](#51-查询某一交易具体信息)
      - [类型](#类型-10)
      - [描述](#描述-10)
      - [请求地址](#请求地址-10)
      - [参数说明](#参数说明-10)
        - [参数介绍](#参数介绍-6)
      - [cURL](#curl-10)
      - [返回值示例](#返回值示例-10)
      - [返回值解析](#返回值解析-10)
    - [5.2 单笔支付](#52-单笔支付)
      - [类型](#类型-11)
      - [描述](#描述-11)
      - [请求地址](#请求地址-11)
      - [参数说明](#参数说明-11)
        - [参数介绍](#参数介绍-7)
        - [参数示例](#参数示例-1)
      - [cURL](#curl-11)
      - [返回值示例](#返回值示例-11)
      - [返回值解析](#返回值解析-11)
    - [5.3 需要sequence的串行批量支付(已移除)](#53-需要sequence的串行批量支付已移除)
      - [类型](#类型-12)
      - [描述](#描述-12)
      - [请求地址](#请求地址-12)
    - [5.4 批量支付](#54-批量支付)
      - [类型](#类型-13)
      - [描述](#描述-13)
      - [请求地址](#请求地址-13)
      - [参数说明](#参数说明-12)
        - [参数介绍](#参数介绍-8)
        - [参数示例](#参数示例-2)
      - [cURL](#curl-12)
      - [返回值示例](#返回值示例-12)
      - [返回值解析](#返回值解析-12)
    - [5.5 签名支付](#55-签名支付)
      - [类型](#类型-14)
      - [描述](#描述-14)
      - [请求地址](#请求地址-14)
      - [参数说明](#参数说明-13)
        - [参数介绍](#参数介绍-9)
        - [参数示例](#参数示例-3)
      - [cURL](#curl-13)
      - [返回值示例](#返回值示例-13)
      - [返回值解析](#返回值解析-13)
    - [5.6 批量签名支付](#56-批量签名支付)
      - [类型](#类型-15)
      - [描述](#描述-15)
      - [请求地址](#请求地址-15)
      - [参数说明](#参数说明-14)
        - [参数介绍](#参数介绍-10)
        - [参数示例](#参数示例-4)
      - [cURL](#curl-14)
      - [返回值示例](#返回值示例-14)
      - [返回值解析](#返回值解析-14)
  - [签名相关](#签名相关)
    - [6.1 服务器签名](#61-服务器签名)
      - [类型](#类型-16)
      - [描述](#描述-16)
      - [请求地址](#请求地址-16)
      - [参数说明](#参数说明-15)
        - [参数介绍](#参数介绍-11)
        - [参数示例](#参数示例-5)
      - [cURL](#curl-15)
      - [返回值示例](#返回值示例-15)
      - [返回值解析](#返回值解析-15)
    - [6.2 服务器批量签名](#62-服务器批量签名)
      - [类型](#类型-17)
      - [描述](#描述-17)
      - [请求地址](#请求地址-17)
      - [参数说明](#参数说明-16)
        - [参数介绍](#参数介绍-12)
        - [参数示例](#参数示例-6)
      - [cURL](#curl-16)
      - [返回值示例](#返回值示例-16)
      - [返回值解析](#返回值解析-16)
  - [安全相关](#安全相关)
    - [说明](#说明-1)
    - [7.1 获取RSA公钥](#71-获取rsa公钥)
      - [类型](#类型-18)
      - [描述](#描述-18)
      - [请求地址](#请求地址-18)
      - [参数说明](#参数说明-17)
        - [参数介绍](#参数介绍-13)
        - [参数示例](#参数示例-7)
      - [cURL](#curl-17)
      - [返回值示例](#返回值示例-17)
      - [返回值解析](#返回值解析-17)
    - [7.2 验证RSA密文的正确性](#72-验证rsa密文的正确性)
      - [类型](#类型-19)
      - [描述](#描述-19)
      - [请求地址](#请求地址-19)
      - [参数说明](#参数说明-18)
        - [参数介绍](#参数介绍-14)
        - [参数示例](#参数示例-8)
      - [cURL](#curl-18)
      - [返回值示例](#返回值示例-18)
      - [返回值解析](#返回值解析-18)
  - [监听事件](#监听事件)
      - [使用说明](#使用说明)
      - [示例网址](#示例网址)
  - [附录](#附录)
    - [附录1:返回值Code说明](#附录1返回值code说明)
  - [更新说明](#更新说明)

<!-- /TOC -->


## 接口文档

### 说明
此系统基于 [SWTC-LIB](https://github.com/swtcca/swtclib/tree/master/docs/swtclib),文档按照各个模块划分,API接口基本和 [SWTC-Proxy](https://swtcdoc.netlify.com/docs/swtcproxy/) 保持一致。


## 服务器相关

### 1.1 创建连接获取服务器基础信息

#### 类型 

GET

#### 描述

创建连接获取服务器基础信息

#### 参数说明

无

#### 请求地址
```
{{host}}/server/info
```
#### cURL

```curl
curl --location --request GET "{{host}}/server/info"
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


### 1.2 请求底层服务器信息

#### 类型 

GET 

#### 描述

创建连接获取底层服务器信息

#### 参数说明

无

#### 请求地址
```
{{host}}/server/node
```
#### cURL

```curl
curl --location --request GET "{{host}}/server/node"
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

## 钱包相关

### 2.1 创建钱包

#### 类型 

GET 

#### 描述

返回创建的钱包

#### 参数说明

无

#### 请求地址
```
{{host}}/wallet/generate
```
#### cURL

```curl
curl --location --request GET "{{host}}/wallet/generate"
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

### 2.2 根据私钥创建钱包

#### 类型 

POST 

#### 描述

根据私钥返回创建钱包的地址

#### 参数说明

##### 参数介绍

| 参数   | 类型    | 说明                                                        |
|--------|---------|-----------------------------------------------------------|
| secret | String  | 井通钱包私钥,如果rsa为'true',则使用加密后的私钥             |
| rsa    | String? | 是否采用RSA加密，加密为'true'，不加密为‘false’ ，默认不加密 |

##### 参数示例

```JSON
{
  "secret":"snXXXXXXXXXXXXXXXXXXXXXXXXXXX",
  "rsa":"false",
}
```

#### 请求地址
```
{{host}}/wallet/generate
```
#### cURL

```curl
curl --location --request POST "{{host}}/wallet/generate" \
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


## 账号相关

### 3.1 请求账号信息

#### 类型 

GET 

#### 描述

请求账号信息


#### 请求地址
```
{{host}}/account/:account/info
```

#### 参数说明

##### 参数介绍

| 参数    | 类型   | 说明         |
|---------|--------|------------|
| account | String | 井通钱包地址 |


#### cURL

```curl
curl --location --request GET "{{host}}/account/:account/info"
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

### 3.2 请求账号余额信息

#### 类型 

GET 

#### 描述

请求账号信息


#### 请求地址
```
{{host}}/account/:account/balances
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
curl --location --request GET "{{host}}/account/:account/balances?currency=CSP&issuer=jGa9J9TkqtBcUoHe2zqhVFFbgUVED6o9or"
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
| data.balances[n].value    | String  | 余额，小数点后六位      |
| data.balances[n].currency | String  | 币种                   |
| data.balances[n].issuer   | String  | 发行商                 |
| data.balances[n].freezed  | String  | 冻结数，小数点后六位    |

### 3.3 获得账号交易列表

#### 类型 

GET 

#### 描述

获得账号交易列表


#### 请求地址
```
{{host}}/account/:account/tx
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
curl --location --request GET "{{host}}/account/:account/tx?limit=10&forward=asc&marker_ledger=14264080&marker_seq=0"
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
| data.transactions[n].date            | Integer | 时间戳                       |
| data.transactions[n].hash            | String  | 交易hash                     |
| data.transactions[n].type            | String  | 交易类型                     |
| data.transactions[n].fee             | String  | 手续费                       |
| data.transactions[n].result          | String  | 交易结果                     |
| data.transactions[n].memos           | Array   | 备注                         |
| data.transactions[n].counterparty    | String  | 交易对家                     |
| data.transactions[n].amount          | Object  | 交易金额对象                 |
| data.transactions[n].amount.value    | String  | 金额                         |
| data.transactions[n].amount.currency | String  | 货币种类                     |
| data.transactions[n].amount.issuer   | String  | 货币                         |
| data.transactions[n].effects         | Array   | 交易效果                     |

## 账本相关

### 4.1 获取最新关闭的账本信息

#### 类型 

GET 

#### 描述

获取最新关闭的账本信息

#### 参数说明

无

#### 请求地址
```
{{host}}/ledgers/closed
```
#### cURL

```curl
curl --location --request GET "{{host}}/ledgers/closed"
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


### 4.2 根据hash获取某一账本具体信息

#### 类型 

GET 

#### 描述

获取某一账本具体信息

#### 请求地址
```
{{host}}/ledgers/hash/:hash
```

#### 参数说明

##### 参数介绍

| 参数         | 类型     | 说明                                              |
|--------------|----------|-------------------------------------------------|
| hash         | String   | 井通区块 hash                                     |
| transactions | Boolean? | 可选参数,是否返回账本上的交易记录 hash，默认 false |

#### cURL

```curl
curl --location --request GET "{{host}}/ledgers/hash/:hash?transactions=true"
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
| data.transactions[n]        | String  | 交易Hash               |

### 4.3 获取某一账本具体信息根据账本高度

#### 类型 

GET 

#### 描述

获取某一账本具体信息

#### 请求地址
```
{{host}}/ledgers/index/:index
```

#### 参数说明

##### 参数介绍

| 参数         | 类型     | 说明                                              |
|--------------|----------|-------------------------------------------------|
| index        | String   | 井通区块高度                                      |
| transactions | Boolean? | 可选参数,是否返回账本上的交易记录 hash，默认 false |

#### cURL

```curl
curl --location --request GET "{{host}}/ledgers/index/:index?transactions=true"
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
| data.transactions[n]        | String  | 交易Hash               |


## 交易事务相关

### 5.1 查询某一交易具体信息

#### 类型 

GET 

#### 描述

查询某一交易具体信息


#### 请求地址
```
{{host}}/tx/:hash
```

#### 参数说明

##### 参数介绍

| 参数 | 类型   | 说明      |
|------|--------|---------|
| hash | String | 交易 hash |


#### cURL

```curl
curl --location --request GET "{{host}}/tx/:hash"
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


### 5.2 单笔支付

#### 类型 

POST 

#### 描述

单笔支付


#### 请求地址
```
{{host}}/tx/pay
```

#### 参数说明

##### 参数介绍

| 参数     | 类型    | 说明                                                        |
|----------|---------|-----------------------------------------------------------|
| account  | String  | 发起账号                                                    |
| to       | String  | 目标账号                                                    |
| value    | String  | 支付数量                                                    |
| currency | String  | 货币种类，三到六个字母或 20 字节的自定义货币                 |
| issuer   | String  | 货币发行方，无则留 ''                                        |
| secret   | String  | 井通钱包私钥,如果rsa为'true',则使用加密后的私钥             |
| rsa      | String? | 是否采用RSA加密，加密为'true'，不加密为‘false’ ，默认不加密 |
| addMemo  | String? | 备注信息                                                    |


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
curl --location --request POST "{{host}}/tx/pay" \
--header "Content-Type: application/json" \
--data "{
	\"account\":\"jJCtKD2MbfYoVdQEbjTmbXmNiVkLBTknLC\",
	\"to\":\"jfAUjEen8cLvRmCGyZYYwumLEZG45PThiR\",
	\"value\":\"0.01\",
	\"currency\":\"SWT\",
	\"issuer\":\"jGa9J9TkqtBcUoHe2zqhVFFbgUVED6o9or\",
	\"secret\":\"snXXXXXXXXXXXXXXXXXXXXXXXXXXX\",
	\"addMemo\":\"测试\"
  \"rsa\":\"false\"
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

### 5.3 需要sequence的串行批量支付(已移除)

#### 类型 

POST 

#### 描述

版本更新后需要支持负载均衡，此接口不支持，所以已移除，不在支持此功能，批量支付请用(5.4)


#### 请求地址
```
{{host}}/tx/serial
```

### 5.4 批量支付

#### 类型 

POST 

#### 描述

批量支付是一个账号在短时间内向多个账号发起交易。因为服务器 sequence 控制比较复杂，所以才有这个接口，系统自动管理sequence。

适用场景：
  1. 新注册用户发放奖励，平台配置一个发放币的账号采用此接口批量转账
  2. 抢红包，并发量大的场景。使用此接口
  3. 收益分发，等分发场景
  4. 新用户激活账户，一个账号给大批账号转SWT的场景
  5. ...


#### 请求地址
```
{{host}}/tx/batch
```

#### 参数说明

##### 参数介绍

| 参数           | 类型    | 说明                                                        |
|----------------|---------|-----------------------------------------------------------|
| account        | String  | 发起账号                                                    |
| secret         | String  | 井通钱包私钥,如果rsa为'true',则使用加密后的私钥             |
| rsa            | String? | 是否采用RSA加密，加密为'true'，不加密为‘false’ ，默认不加密 |
| tx             | Array   | 需要交易的地址对                                            |
| tx[n].to       | String  | 目标账号                                                    |
| tx[n].value    | String  | 支付数量                                                    |
| tx[n].currency | String  | 货币种类，三到六个字母或 20 字节的自定义货币                 |
| tx[n].issuer   | String  | 货币发行方，无则留 ''                                        |
| tx[n].addMemo  | String? | 备注信息                                                    |

##### 参数示例

```JSON
{
  "account":"jJCtKD2MbfYoVdQEbjTmbXmNiVkLBTknLC",
  "secret":"snXXXXXXXXXXXXXXXXXXXXXXXXXXX",
  "rsa":"false",
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
curl --location --request POST "{{host}}/tx/batch" \
--header "Content-Type: application/json" \
--data "{
  \"account\":\"jJCtKD2MbfYoVdQEbjTmbXmNiVkLBTknLC\",
  \"secret\":\"snXXXXXXXXXXXXXXXXXXXXXXXXXXX\",
  \"rsa\":\"false\",
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
| data[n].success                    | String  | 这一笔交易在提交到公共节点上是否有错误 |
| data[n].msg                        | String  | 这一笔交易在提交到公共节点上的提示信息 |
| data[n].index                      | String  | 每一笔在整个交易数组中的底标           |
| data[n].data                       | Array   | SWTC-LIB 返回的精简数据                |
| data[n].data.engine_result         | String  | 请求结果，根据是否为tesSUCCESS判断成功  |
| data[n].data.engine_result_code    | Integer | 请求结果编码                           |
| data[n].data.engine_result_message | String  | 请求结果 message 信息                  |
| data[n].data.Sequence              | Integer | 单子序列号                             |
| data[n].data.hash                  | String  | 交易 hash                              |

### 5.5 签名支付

#### 类型 

POST 

#### 描述

签名支付


#### 请求地址
```
{{host}}/tx/blob
```

#### 参数说明

##### 参数介绍

| 参数 | 类型   | 说明         |
|------|--------|------------|
| blob | String | 签名后的blob |

##### 参数示例

```JSON
{
  "blob":"120000220000000024000018B261D4038D7EA4C680000000000000000000000000544553540000000000A582E432BFC48EEDEF852C814EC57F3CD2D4159668400000000000271073210256F9ED0A13D879E2DAC205A23CF1BA6DA210C094F3B18168945BBCD0664BAD0C74473045022100ACD6B696B480AF42B929101FEDDA2B72FE36553415A12A41E3CBA770EBE4F616022047744119D76D9F700ED64705A4EEFD0929C7511D1865002A7611CC66548580BD8114C1D4C79B2C9CD8FE9AB1EE29FAA18432A3DBFD8A83140D2C803B102F69C7AF902747C0CE6B0C90CF869A"
}
```

#### cURL

```curl
curl --location --request POST '{{host}}/tx/blob' \
--header 'Content-Type: application/x-www-form-urlencoded' \
--data-urlencode 'blob=120000220000000024000018B261D4038D7EA4C680000000000000000000000000544553540000000000A582E432BFC48EEDEF852C814EC57F3CD2D4159668400000000000271073210256F9ED0A13D879E2DAC205A23CF1BA6DA210C094F3B18168945BBCD0664BAD0C74473045022100ACD6B696B480AF42B929101FEDDA2B72FE36553415A12A41E3CBA770EBE4F616022047744119D76D9F700ED64705A4EEFD0929C7511D1865002A7611CC66548580BD8114C1D4C79B2C9CD8FE9AB1EE29FAA18432A3DBFD8A83140D2C803B102F69C7AF902747C0CE6B0C90CF869A'
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
        "tx_blob": "120000220000000024000018B461D4038D7EA4C680000000000000000000000000544553540000000000A582E432BFC48EEDEF852C814EC57F3CD2D4159668400000000000271073210256F9ED0A13D879E2DAC205A23CF1BA6DA210C094F3B18168945BBCD0664BAD0C74473045022100EBF00D6DA4AFABD85871EE8779A020D52D8F424C221AA657830F28E1FE6BCE20022060E33DB8A6B54E9F1A2EA236D7BBDDF031AD0269FE56910B8180E7D48A6D601A8114C1D4C79B2C9CD8FE9AB1EE29FAA18432A3DBFD8A83140D2C803B102F69C7AF902747C0CE6B0C90CF869AF9EA7D06E6B58BE8AF95E1F1",
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
            "Sequence": 6324,
            "SigningPubKey": "0256F9ED0A13D879E2DAC205A23CF1BA6DA210C094F3B18168945BBCD0664BAD0C",
            "TransactionType": "Payment",
            "TxnSignature": "3045022100EBF00D6DA4AFABD85871EE8779A020D52D8F424C221AA657830F28E1FE6BCE20022060E33DB8A6B54E9F1A2EA236D7BBDDF031AD0269FE56910B8180E7D48A6D601A",
            "hash": "9EF75982726A5B32EC8417C3D3427572DA6342C50D39A83A47D68CD22181A9C6"
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

### 5.6 批量签名支付

#### 类型 

POST 

#### 描述

批量签名支付


#### 请求地址
```
{{host}}/tx/batchblob
```

#### 参数说明

此接口内部的blob是按照（6.2）批量签名返回的顺序进行提交，blob内部带有sequence的序列，请组装的时候也必须按照顺序进行组装使用

##### 参数介绍

| 参数           | 类型   | 说明             |
|----------------|--------|----------------|
| txBlob         | Array  | 签名后的blob数组 |
| txBlob[n].blob | String | 签名后的blob     |

##### 参数示例

```JSON
{
    "txBlob": [
        {
            "blob": "120000220000000024000018AF61D4038D7EA4C680000000000000000000000000544553540000000000A582E432BFC48EEDEF852C814EC57F3CD2D4159668400000000000271073210256F9ED0A13D879E2DAC205A23CF1BA6DA210C094F3B18168945BBCD0664BAD0C74463044022024146703D92E1597492600044E42AD5C4428BA90FA5249B70C59B03A3BC797730220394577D634D37670F372035A04B764903E9824D089A22E4132BDAF5B5AAE090A8114C1D4C79B2C9CD8FE9AB1EE29FAA18432A3DBFD8A83140D2C803B102F69C7AF902747C0CE6B0C90CF869AF9EA7D07E6B58BE8AF9531E1F1"
        },
        {
            "blob": "120000220000000024000018B061D4038D7EA4C680000000000000000000000000544553540000000000A582E432BFC48EEDEF852C814EC57F3CD2D4159668400000000000271073210256F9ED0A13D879E2DAC205A23CF1BA6DA210C094F3B18168945BBCD0664BAD0C7446304402205E6919EC4C0A61FB8B76A86BAA28C6D5012E77DFB5C4248615C6428B8E2A7D1902203C2F69C56E5F6EA6CFC69718F55F6BEC133EBB73ACE18EA5AA0F4EBD64AE49A28114C1D4C79B2C9CD8FE9AB1EE29FAA18432A3DBFD8A83140D2C803B102F69C7AF902747C0CE6B0C90CF869AF9EA7D07E6B58BE8AF9532E1F1"
        },
        {
            "blob": "120000220000000024000018B161D4038D7EA4C680000000000000000000000000544553540000000000A582E432BFC48EEDEF852C814EC57F3CD2D4159668400000000000271073210256F9ED0A13D879E2DAC205A23CF1BA6DA210C094F3B18168945BBCD0664BAD0C74473045022100BC123E3CFFCEBE37E0B7D62D80501ACA0CD9D8E16DC0A7A0CE3FBAF2BE04BCE7022067674CBF1288F5AFD938B4F4A11D87AADDFF1C1C7E3415B1BEFF60EE44A7516B8114C1D4C79B2C9CD8FE9AB1EE29FAA18432A3DBFD8A83140D2C803B102F69C7AF902747C0CE6B0C90CF869A"
        }
    ]
}
```

#### cURL

```curl
curl --location --request POST '{{host}}/tx/batchblob' \
--header 'Content-Type: application/json' \
--data-raw '{
    "txBlob": [
        {
            "blob": "120000220000000024000018AF61D4038D7EA4C680000000000000000000000000544553540000000000A582E432BFC48EEDEF852C814EC57F3CD2D4159668400000000000271073210256F9ED0A13D879E2DAC205A23CF1BA6DA210C094F3B18168945BBCD0664BAD0C74463044022024146703D92E1597492600044E42AD5C4428BA90FA5249B70C59B03A3BC797730220394577D634D37670F372035A04B764903E9824D089A22E4132BDAF5B5AAE090A8114C1D4C79B2C9CD8FE9AB1EE29FAA18432A3DBFD8A83140D2C803B102F69C7AF902747C0CE6B0C90CF869AF9EA7D07E6B58BE8AF9531E1F1"
        },
        {
            "blob": "120000220000000024000018B061D4038D7EA4C680000000000000000000000000544553540000000000A582E432BFC48EEDEF852C814EC57F3CD2D4159668400000000000271073210256F9ED0A13D879E2DAC205A23CF1BA6DA210C094F3B18168945BBCD0664BAD0C7446304402205E6919EC4C0A61FB8B76A86BAA28C6D5012E77DFB5C4248615C6428B8E2A7D1902203C2F69C56E5F6EA6CFC69718F55F6BEC133EBB73ACE18EA5AA0F4EBD64AE49A28114C1D4C79B2C9CD8FE9AB1EE29FAA18432A3DBFD8A83140D2C803B102F69C7AF902747C0CE6B0C90CF869AF9EA7D07E6B58BE8AF9532E1F1"
        },
        {
            "blob": "120000220000000024000018B161D4038D7EA4C680000000000000000000000000544553540000000000A582E432BFC48EEDEF852C814EC57F3CD2D4159668400000000000271073210256F9ED0A13D879E2DAC205A23CF1BA6DA210C094F3B18168945BBCD0664BAD0C74473045022100BC123E3CFFCEBE37E0B7D62D80501ACA0CD9D8E16DC0A7A0CE3FBAF2BE04BCE7022067674CBF1288F5AFD938B4F4A11D87AADDFF1C1C7E3415B1BEFF60EE44A7516B8114C1D4C79B2C9CD8FE9AB1EE29FAA18432A3DBFD8A83140D2C803B102F69C7AF902747C0CE6B0C90CF869A"
        }
    ]
}'
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
                "sequence": 6325,
                "hash": "3308120268ADE1D2EB44382DCE024E2E8C12E0BB9D15D8A3B3B6AC01B6259E00"
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
                "sequence": 6326,
                "hash": "4BC4AE3D35BFA70C8C4C5669CD898D00D422D921B65C969BCA8A492EDEF0032F"
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
                "sequence": 6327,
                "hash": "04734C94EB67B9E92DDBB59C93F7456A53EE19E218090BBC9BB2EEFFB2C2688E"
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
| data[n].success                    | String  | 这一笔交易在提交到公共节点上是否有错误 |
| data[n].msg                        | String  | 这一笔交易在提交到公共节点上的提示信息 |
| data[n].index                      | String  | 每一笔在整个交易数组中的底标           |
| data[n].data                       | Array   | SWTC-LIB 返回的精简数据                |
| data[n].data.engine_result         | String  | 请求结果，根据是否为tesSUCCESS判断成功  |
| data[n].data.engine_result_code    | Integer | 请求结果编码                           |
| data[n].data.engine_result_message | String  | 请求结果 message 信息                  |
| data[n].data.Sequence              | Integer | 单子序列号                             |
| data[n].data.hash                  | String  | 交易 hash                              |

## 签名相关

### 6.1 服务器签名

#### 类型 

POST 

#### 描述

本地签名的服务器端解决方案，此接口支持指定Sequence。

#### 请求地址
```
{{host}}/sign/pay
```

#### 参数说明

##### 参数介绍

| 参数     | 类型    | 说明                                                        |
|----------|---------|-----------------------------------------------------------|
| account  | String  | 发起账号                                                    |
| to       | String  | 目标账号                                                    |
| value    | String  | 支付数量                                                    |
| currency | String  | 货币种类，三到六个字母或 20 字节的自定义货币                 |
| issuer   | String  | 货币发行方，无则留 ''                                        |
| secret   | String  | 井通钱包私钥,如果rsa为'true',则使用加密后的私钥             |
| rsa      | String? | 是否采用RSA加密，加密为'true'，不加密为‘false’ ，默认不加密 |
| addMemo  | String? | 备注信息                                                    |
| sequence | String? | 此次签名里面添加的sequence，不传则是默认下一次的sequence     |

##### 参数示例

```JSON
{
	"account":"jJCtKD2MbfYoVdQEbjTmbXmNiVkLBTknLC",
	"to":"jfAUjEen8cLvRmCGyZYYwumLEZG45PThiR",
	"value":"0.01",
	"currency":"SWT",
	"issuer":"jGa9J9TkqtBcUoHe2zqhVFFbgUVED6o9or",
	"secret":"snXXXXXXXXXXXXXXXXXXXXXXXXXXX",
  "addMemo":"测试",
  "sequence":"6285",
  "rsa":"false"
}
```

#### cURL

```curl
curl --location --request POST "{{host}}/tx/pay" \
--header "Content-Type: application/json" \
--data "{
	\"account\":\"jJCtKD2MbfYoVdQEbjTmbXmNiVkLBTknLC\",
	\"to\":\"jfAUjEen8cLvRmCGyZYYwumLEZG45PThiR\",
	\"value\":\"0.01\",
	\"currency\":\"SWT\",
	\"issuer\":\"jGa9J9TkqtBcUoHe2zqhVFFbgUVED6o9or\",
	\"secret\":\"snXXXXXXXXXXXXXXXXXXXXXXXXXXX\",
	\"addMemo\":\"测试\",
  \"sequence\":\"6285\",
  \"rsa\":\"false\",
}"
```
#### 返回值示例

```JSON
{
    "success": true,
    "msg": "请求成功",
    "code": 0,
    "data": "120000220000000024000018B861D4038D7EA4C680000000000000000000000000544553540000000000A582E432BFC48EEDEF852C814EC57F3CD2D4159668400000000000271073210256F9ED0A13D879E2DAC205A23CF1BA6DA210C094F3B18168945BBCD0664BAD0C74463044022016586A1E27F5882B769864219485E3412B3DF47D02FAF46CA90CB8D0A9A4959302204201C5E4BC94C10A4645FB50B1175B0B2D1E4062C9D36C90C869C0A35F2FA4AA8114C1D4C79B2C9CD8FE9AB1EE29FAA18432A3DBFD8A83140D2C803B102F69C7AF902747C0CE6B0C90CF869AF9EA7D06E6B58BE8AF95E1F1"
}
```
#### 返回值解析

| 参数    | 类型    | 说明                   |
|---------|---------|----------------------|
| success | Boolean | 此次请求是否成功       |
| msg     | String  | 返回的信息             |
| code    | Integer | 服务器返回的请求状态码 |
| data    | String  | 签名信息               |

### 6.2 服务器批量签名

#### 类型 

POST 

#### 描述

服务器批量签名，此接口默认后台会获取到sequence，不需要自行管理


#### 请求地址
```
{{host}}/sign/batch
```

#### 参数说明

##### 参数介绍

| 参数           | 类型    | 说明                                                        |
|----------------|---------|-----------------------------------------------------------|
| account        | String  | 发起账号                                                    |
| secret         | String  | 井通钱包私钥,如果rsa为'true',则使用加密后的私钥             |
| rsa            | String? | 是否采用RSA加密，加密为'true'，不加密为‘false’ ，默认不加密 |
| tx             | Array   | 需要交易的地址对                                            |
| tx[n].to       | String  | 目标账号                                                    |
| tx[n].value    | String  | 支付数量                                                    |
| tx[n].currency | String  | 货币种类，三到六个字母或 20 字节的自定义货币                 |
| tx[n].issuer   | String  | 货币发行方，无则留 ''                                        |
| tx[n].addMemo  | String? | 备注信息                                                    |

##### 参数示例

```JSON
{
  "account":"jJCtKD2MbfYoVdQEbjTmbXmNiVkLBTknLC",
  "secret":"snXXXXXXXXXXXXXXXXXXXXXXXXXXX",
  "rsa":"false",
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
curl --location --request POST "{{host}}/sign/batch" \
--header "Content-Type: application/json" \
--data "{
  \"account\":\"jJCtKD2MbfYoVdQEbjTmbXmNiVkLBTknLC\",
  \"secret\":\"snXXXXXXXXXXXXXXXXXXXXXXXXXXX\",
  \"rsa\":\"false\",
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
        "120000220000000024000018B561D4038D7EA4C680000000000000000000000000544553540000000000A582E432BFC48EEDEF852C814EC57F3CD2D4159668400000000000271073210256F9ED0A13D879E2DAC205A23CF1BA6DA210C094F3B18168945BBCD0664BAD0C7446304402203454942369C11B47AE13CCE10BE600FE3286523DC03F678B579FBEE214A3BE6E0220761D4AAA976F0065622C1BE27F8B6DDAA047CEBFBFB9B4A99DEFBEC9C210D3028114C1D4C79B2C9CD8FE9AB1EE29FAA18432A3DBFD8A83140D2C803B102F69C7AF902747C0CE6B0C90CF869AF9EA7D07E6B58BE8AF9531E1F1",
        "120000220000000024000018B661D4038D7EA4C680000000000000000000000000544553540000000000A582E432BFC48EEDEF852C814EC57F3CD2D4159668400000000000271073210256F9ED0A13D879E2DAC205A23CF1BA6DA210C094F3B18168945BBCD0664BAD0C74463044022050398377192CEBA0B6941E3EC00E2C7DEC256F3F00939B0EFF2464BE6734D1FF02207C6729C570E379E0A82E6A90E0A5E786A4DFBADF138123C846B5D4487F1EFAB38114C1D4C79B2C9CD8FE9AB1EE29FAA18432A3DBFD8A83140D2C803B102F69C7AF902747C0CE6B0C90CF869AF9EA7D07E6B58BE8AF9532E1F1",
        "120000220000000024000018B761D4038D7EA4C680000000000000000000000000544553540000000000A582E432BFC48EEDEF852C814EC57F3CD2D4159668400000000000271073210256F9ED0A13D879E2DAC205A23CF1BA6DA210C094F3B18168945BBCD0664BAD0C7446304402207A8F843FBD1E235E3F53252F217A486B8F8C049A50BDAEBB81E3B1E231199E1E02205980D4BD55EC2EA7DF67F6BFF54090FBD861A5F1E9A37F2ADC47FC0B058AF5648114C1D4C79B2C9CD8FE9AB1EE29FAA18432A3DBFD8A83140D2C803B102F69C7AF902747C0CE6B0C90CF869A"
    ]
}
```

#### 返回值解析

| 参数    | 类型    | 说明                         |
|---------|---------|----------------------------|
| success | Boolean | 此次请求是否成功             |
| msg     | String  | 返回的信息                   |
| code    | Integer | 服务器返回的请求状态码       |
| data    | Array   | 每一笔签名提交返回的签名数组 |
| data[n] | String  | 对应的签名信息               |

## 安全相关

### 说明

一、 为了私钥的安全性，SWTCLIB-APP采用了加密私钥传输的方案。遵循以下几个原则

* 私钥不出本机
* 私钥不在网络流通
* 服务器不存储任何私钥信息
* 所有需要传递私钥的接口都支持两种方式：
  1. RSA加密进行安全传输
  2. 默认的明文传输方式

二、 加密方式

* 加密方式为 RSA PKCS8 1024 非对称加密
* 服务器存储公钥和私钥，并把公钥公布给客户端
* 客户端获取公钥之后，请按照加密方案进行加密

三、 进行验证

* 系统提供一个接口来验证加密后的结果是否和原文一致，只是验证一致性
* 可以通过其他需要私钥的接口进行操作验证

### 7.1 获取RSA公钥

#### 类型 

GET 

#### 描述

获取最新可用的RSA公钥

#### 请求地址
```
{{host}}/rsa/public
```

#### 参数说明

无

##### 参数介绍

无

##### 参数示例

无

#### cURL

```curl
curl --location --request GET '{{host}}/rsa/public'
```
#### 返回值示例

```JSON
{
    "success": true,
    "msg": "请求成功",
    "code": 0,
    "data": "-----BEGIN RSA PUBLIC KEY-----\nMEgCQQCTXpw3qIlY0RQb1nEF7l1ZHFd94HlM+FF6LBThXNvZ2QjfqkxOvwiORsnh\nMP3YCLYf2CgUR6ywMukI16CGU1JJAgMBAAE=\n-----END RSA PUBLIC KEY-----"
}
```
#### 返回值解析

| 参数    | 类型    | 说明                   |
|---------|---------|----------------------|
| success | Boolean | 此次请求是否成功       |
| msg     | String  | 返回的信息             |
| code    | Integer | 服务器返回的请求状态码 |
| data    | String  | 最新的公钥信息         |

### 7.2 验证RSA密文的正确性

#### 类型 

POST 

#### 描述

验证客户端提供的明文和密文是否对应

#### 请求地址
```
{{host}}/rsa/verify
```

#### 参数说明

##### 参数介绍

| 参数       | 类型   | 说明                    |
|------------|--------|-----------------------|
| plaintext  | String | 明文                    |
| ciphertext | String | 使用RSA公钥加密后的密文 |

##### 参数示例

```JSON
{
  "plaintext":"jfTqijsayy6W8uNB3FQCV2N5HzbApWBBs6",
  "ciphertext":"XUMgOP5O85PIjSSSHejZIFRwkcSCNq+vqGKDeDKdqleCEj5NO45oEd05ETt9xU9ZFWb2Uj06mH+6kk26yIb42DLbw0+6JV2uyesT1rGAzwJvOpxOhnq5qlHBtu3f6rQCMBS5i0Go3BI+RdXAl8WD67IW2wryGfE3AxB/wk2TpR0=",
}
```

#### cURL

```curl
curl --location --request POST '{{host}}/rsa/verify' \
--header 'Content-Type: application/x-www-form-urlencoded' \
--data-urlencode 'plaintext=jfTqijsayy6W8uNB3FQCV2N5HzbApWBBs6' \
--data-urlencode 'ciphertext=XUMgOP5O85PIjSSSHejZIFRwkcSCNq+vqGKDeDKdqleCEj5NO45oEd05ETt9xU9ZFWb2Uj06mH+6kk26yIb42DLbw0+6JV2uyesT1rGAzwJvOpxOhnq5qlHBtu3f6rQCMBS5i0Go3BI+RdXAl8WD67IW2wryGfE3AxB/wk2TpR0='
```
#### 返回值示例

```JSON
{
    "success": true,
    "msg": "请求成功",
    "code": 0,
    "data": null
}
// 或者
{
    "success": false,
    "msg": "公钥或加密方式不对!",
    "code": 400000,
    "data": null
}
```

#### 返回值解析

| 参数    | 类型    | 说明                   |
|---------|---------|----------------------|
| success | Boolean | 此次请求是否成功       |
| msg     | String  | 返回的信息             |
| code    | Integer | 服务器返回的请求状态码 |

## 监听事件

目前支持两个监听事件:
- 监听所有交易(transactions)
- 监听所有账本(ledger_closed)

监听结果为标准的websocket返回信息。

#### 使用说明

使用的是标准WS链接，测试地址为 ws://152.136.110.80

监听如下两个事件：
- transactions
- ledger_closed

#### 示例网址

[点击访问](http://152.136.110.80/socket/swtc-socket-test/1.html)

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

## 更新说明

[更新详细信息](./UPDATE.md)