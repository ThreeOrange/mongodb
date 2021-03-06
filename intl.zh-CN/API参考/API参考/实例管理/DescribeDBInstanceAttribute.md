# DescribeDBInstanceAttribute {#reference_g3m_t44_k2b .reference}

## 描述 {#section_idp_r44_k2b .section}

该接口用于查询实例详情，支持副本集实例和分片集群实例。

## 输入参数 {#section_k5t_t44_k2b .section}

|名称|类型|是否必须|描述|
|--|--|----|--|
|Action|String|是|系统规定参数，取值为：DescribeDBInstanceAttribute。|
|DBInstanceId|String|是|实例ID，可一次输入多个，以英文“,”逗号分隔，最多传入30个。|

## 返回参数 {#section_m5j_w44_k2b .section}

|名称|类型|描述|
|--|--|--|
|公共返回参数|-|详见[ZH-CN\_TP\_6765.md\#](intl.zh-CN/.md#)。|
|DBInstances|List<DBInstance\>|-|
|MaintainStartTime|String|可运维时间段的开始时间，格式：HH:mmZ ，如：01:00Z。|
|MaintainEndTime|String|可运维时间段的结束时间，格式： HH:mmZ ，如：02:00Z。|

## DBInstance的参数 {#section_idp_r44_k2b2 .section}

|名称|类型|描述|
|--|--|--|
|DBInstanceId|String|实例ID。|
|DBInstanceDescription|String|实例描述。|
|RegionId|String|实例所属地域ID。|
|ZoneId|String|实例所属可用区ID。|
|Engine|String|数据库类型。|
|EngineVersion|String|数据库版本。|
|DBInstanceClass|String|实例规格。|
|DBInstanceStorage|String|实例存储空间。|
|DBInstanceStatus|String|实例状态，请参见[实例状态表](https://www.alibabacloud.com/help/zh/doc-detail/63870.htm)。|
|ChargeType|String|付费类型：-   PrePaid：包年包月；
-   PostPaid：按量付费。

|
|ReplicaSetName|String|副本集实例名称。|
|CreationTime|String|实例创建时间。|
|ExpireTime|String|包年包月实例到期时间，按量付费实例无到期时间。|
|MaintainStartTime|String|实例可维护时间段的开始时间。|
|MaintainEndTime|String|实例可维护时间段的结束时间。|
|NetworkType|String|实例的网络类型：-   Classic：经典网络；
-   VPC：VPC网络。

|
|DBInstanceType|String|实例类型-   sharding：集群版实例；
-   replicate：副本集实例。

|
|LastDowngradeTime|Integer|实例最近一次降配时间。|
|MongosList|List<MongosAttribute\>|Mongos的列表，当DBInstanceType为sharding时，该参数有返回值。|
|ShardList|List<ShardAttribute\>|Shard的列表，当DBInstanceType为sharding时，该参数有返回值。|

## MongosAttribute的参数 {#section_nyc_fyp_k2b .section}

|名称|类型|描述|
|--|--|--|
|NodeId|String|Mongos的实例ID。|
|NodeDescription|String|Mongos的实例描述。|
|NodeClass|String|Mongos的实例规格。|
|ConnectSting|String|Mongos的实例连接串。|
|Port|String|Mongos的实例端口。|

## ShardAttribute的参数 {#section_xqn_kyp_k2b .section}

|名称|类型|描述|
|--|--|--|
|NodeId|String|Shard的实例ID。|
|NodeDescription|String|Shard的实例描述。|
|NodeClass|String|Shard的实例规格。|
|OrderId|String|订单ID。|
|NodeStorage|String|Shard的存储空间。|

