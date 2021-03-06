# Event::onGatewayConnect
**(```WorkerMan>=2.0，Gateway/Worker模型```)**

## 说明:
```php
void Gateway::onGatewayConnect(int $client_id);
```

当客户端连接上gateway进程时触发。例如客户端连接到gateway进程后，服务端要向新连接的客户端发送一个token，客户端需要根据token计算登录的凭证，然后通过这个凭证向服务端发起登录请求。

绝大多数应用在不用实现这个函数。

## 参数
(WorkerMan>=2.1.3)

``` $client_id ```
全局唯一的客户端socket_id

## 返回值
无返回值，任何返回值都会被视为无效的


## 范例
```php
use \Lib\Gateway;

public onGatewayConnect($client)
{
   // 客户端一旦连接到服务端，服务端便向客户端发送一个token
   // 客户端根据这个token数据生成登录请求凭证
   $salt = '!@#$%^';
   Gateway::sendToCurrentClient('token='.md5(time().$salt));
}

```
