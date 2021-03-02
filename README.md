Django HTTP Proxy 
=================

### django 代理服务，格式为 url('proxy/(?P<http>\d+)/(?P<url>.*)', proxy_view),  http为1时表示是http协议  0为https协议
加入了crsf，避免跨域问题

#### http代理访问地址为  https://xxx/proxy/1/www.baidu.com/
#### https代理访问地址为  https://xxx/proxy/0/www.baidu.com/

## 完全支持put post 等方法带参

Installation
============

Install with

```console
$ pip install django-proxy-crsf
```

Overview
========

Forward as close to an exact copy of the request as possible along to a
given url.  Respond with as close to an exact copy of the resulting
response as possible.

Includes a view function that can be used directly from a URL spec:

```python
from proxy.views import proxy_view

urlpatterns = patterns(
	...
                url('proxy/(?P<http>\d+)/(?P<url>.*)', proxy_view),
	...
)
```

License
=======

Copyright © blackjack0v0

All rights reserved.

