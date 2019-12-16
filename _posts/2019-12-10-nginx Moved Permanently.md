---
title: nginx Moved Permanently
tags: [Server, nginx]
style: fill
color: light
description: nginx에서 http 접속 시 https로 Redirect시키는 방법
---

### nginx에서 301 Moved Permanently 응답 보내는 방법

설정 파일을 연다.

```bash
vi /etc/nginx/sites-available/default
```

return 구문을 추가한다.

```bash
server
{
	listen	80;
	...
	return 301 https://$host$request_uri;
}
```

완료.
