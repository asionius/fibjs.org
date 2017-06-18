# 模块 uuid
uuid 唯一 id 模块

基础模块。提供唯一 id 的创建于操作
```JavaScript
var uuid = require('uuid');
```
## 函数
        
### node
使用时间和主机名创建 uuid
```JavaScript
static Buffer uuid.node();
```

返回结果:
* 返回一个生成的二进制 id

--------------------------
### md5
使用特定命名的 md5 创建 uuid
```JavaScript
static Buffer uuid.md5(Integer ns,
                String name);
```

调用参数:
* ns - 指定命名空间，可以为 uuid.DNS, uuid.URL, uuid.OID, uuid.X509
* name - 指定名称

返回结果:
* 返回一个生成的二进制 id

--------------------------
### random
使用随机数创建 uuid
```JavaScript
static Buffer uuid.random();
```

返回结果:
* 返回一个生成的二进制 id

--------------------------
### sha1
使用特定命名的 sha1 创建 uuid
```JavaScript
static Buffer uuid.sha1(Integer ns,
                String name);
```

调用参数:
* ns - 指定命名空间，可以为 uuid.DNS, uuid.URL, uuid.OID, uuid.X509
* name - 指定名称

返回结果:
* 返回一个生成的二进制 id

--------------------------
### snowflake
使用 Snowflake 算法创建 uuid
```JavaScript
static Buffer uuid.snowflake();
```

返回结果:
* 返回一个生成的二进制 id

## 属性
        
### hostID
查询和修改 Snowflake 算法的主机 id
```JavaScript
static Integer uuid.hostID;
```

## 常量
        
### DNS
md5 与 sha1 创建 uuid 时指定 name 命名为域名
```JavaScript
const uuid.DNS = 0;
```

--------------------------
### URL
md5 与 sha1 创建 uuid 时指定 name 命名为 [url](url.md) 地址
```JavaScript
const uuid.URL = 1;
```

--------------------------
### OID
md5 与 sha1 创建 uuid 时指定 name 命名为 ISO OID
```JavaScript
const uuid.OID = 2;
```

--------------------------
### X509
md5 与 sha1 创建 uuid 时指定 name 命名为 X.500 DN
```JavaScript
const uuid.X509 = 3;
```
