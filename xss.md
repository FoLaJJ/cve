# payroll-management-system-in-php has Cross Site Scripting vulnerability in home_employee.php

## supplier 
https://code-projects.org/payroll-management-system-in-php-with-source-code/
## Vulnerability file
home_employee.php
## describe
There is an  Cross Site Scripting vulnerability in blood-bank-system-in-php  in home_employee.php. Control parameter: $division

A malicious attacker can use this vulnerability to obtain administrator login credentials or phishing websites

## code analysis

In home_employee.php，get $row['division'], and echo it in no filter.

![Image](https://github.com/user-attachments/assets/117a4454-b7a8-4a86-a321-0efb8e023fa7)

## POC

```
GET /home_employee.php HTTP/1.1
Host: payroll
Cache-Control: max-age=0
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/122.0.6261.112 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7
Accept-Encoding: gzip, deflate, br
Accept-Language: zh-CN,zh;q=0.9
Cookie: PHPSESSID=85u4m47klj7ldjr47mclti8mr6
Connection: close


```

**Result**

![Image](https://github.com/user-attachments/assets/a8dad9ab-9a32-4d10-94e5-05235530fb54)
