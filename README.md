Django HTTP Proxy 
=================
**Simple HTTP proxy service as a Django app.**
django 代理服务，格式为 url('proxy/(?P<http>\d+)/(?P<url>.*)', proxy_view),  http为1时表示是http协议  0为https协议
加入了crsf，避免跨域问题

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

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:

Redistributions of source code must retain the above copyright notice, this
list of conditions and the following disclaimer.
Redistributions in binary form must reproduce the above copyright notice, this
list of conditions and the following disclaimer in the documentation and/or
other materials provided with the distribution.
THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND
ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED
WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE
FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

