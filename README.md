mysite.com
===

Apache2 setup
---
```
WSGIScriptAlias / /home/ubuntu/mysite.com/mysite/wsgi.py
WSGIPythonPath /home/ubuntu/mysite.com

<VirtualHost *:80>
  <Directory /home/ubuntu/mysite.com/mysite>
    <Files wsgi.py>
      Order deny,allow
      Allow from all
    </Files>
  </Directory>
</VirtualHost>
```