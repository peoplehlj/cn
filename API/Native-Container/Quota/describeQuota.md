# describeQuota


## 描述
查询资源的配额

## 请求方式
GET

## 请求地址
https://nc.jdcloud-api.com/v1/regions/{regionId}/quotas

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**regionId**|String|True||Region ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**resourceType**|String|True||资源类型  container：用户能创建的容器的配额  secret：用户能创建的secret的配额|


## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String||
|**result**|[Result](##Result)||


### <a name="Result">Result</a>
|名称|类型|描述|
|---|---|---|
|**quota**|[Quota](##Quota)||
### <a name="Quota">Quota</a>
|名称|类型|描述|
|---|---|---|
|**limit**|Integer|配额|
|**used**|Integer|已使用的数目|

## 返回码
|返回码|描述|
|---|---|
|**400**|Invalid parameter|
|**401**|Authentication failed|
|**404**|Not found|
|**503**|Service unavailable|
|**200**|OK|
|**500**|Internal server error|
