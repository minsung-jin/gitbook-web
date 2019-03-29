# httpd.conf 설정

## Apache HTTP 서버에 외부 폴더 추가

* Server root
```
Define SRVROOT "C:/Users/minsung/workspace/httpd/Apache24"
```
* Load mod_alias
```
LoadModule alias_module modules/mod_alias.so
```
* Alias
~~~
Alias [가상 주소] [실제 파일 위치]
~~~
```
Alias /study "C:/Users/minsung/workspace/git/study"
```
* Directory
~~~
<Directory [실제 파일 위치]>
[옵션]
</Directory>
~~~
```
<Directory "C:/Users/minsung/workspace/">
Options Indexes FollowSymLinks
AllowOverride None
Require all granted
</Directory>
<code>
```