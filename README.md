# Xdecrypt

Xshell Xftp 密码解密查看
长时间通过软件保存的密码自动连接, 久了就忘了 

## Setup
```
pip3 install -r requirements.txt
```

## Usage
```
usage: Xdecrypt.py [-h] [-s SID] [-p PASSWORD]

xsh, xfp password decrypt

optional arguments:
  -h, --help            show this help message and exit
  -s SID, --sid SID     `username`+`sid`, user `whoami /user` in command.
  -p PASSWORD, --password PASSWORD
                        the password in sessions or path of sessions
```

```
$ whoami /user
用户信息
----------------

用户名               SID
==================== =============================================
computername\username sid

$ python3 Xdecrypt.py
=============C:\Users\yourname\Documents\NetSarang Computer\6\Xftp\Sessions\192.168.1.2.xfp=============
Host:     192.168.1.2:22
Username: root
Password: test
==========C:\Users\d2x3\Documents\NetSarang Computer\6\Xshell\Sessions\192.168.1.2.xsh===========
Host:     192.168.1.2:22
Username: root
Password: test
========C:\Users\d2x3\Documents\NetSarang Computer\6\Xshell\Sessions\test\192.168.1.2.xsh========
Host:     192.168.1.2:22
Username: root
Password: test

$ python3 Xdecrypt.py -s username+sid -p "D:\somewhere\NetSarang Computer"
=============D:\somewhere\NetSarang Computer\6\Xftp\Sessions\192.168.1.2.xfp=============
Host:     192.168.1.2:22
Username: root
Password: test
==========D:\somewhere\NetSarang Computer\6\Xshell\Sessions\192.168.1.2.xsh===========
Host:     192.168.1.2:22
Username: root
Password: test
========D:\somewhere\NetSarang Computer\6\Xshell\Sessions\test\192.168.1.2.xsh========
Host:     192.168.1.2:22
Username: root
Password: test

$ python Xdecrypt.py -s username+sid -p password
test
```
