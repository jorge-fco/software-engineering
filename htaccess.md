# .htaccess:
_Hypertext Access_. Archivo de configuración para servidores web basados en Apache.

### Remove (www) from my domain
```
RewriteEngine On
RewriteCond %{HTTP_HOST} ^www\.(.*)$ [NC]
RewriteRule ^(.*)$ http://%1%{REQUEST_URI} [R=301,QSA,NC,L]
```

### Remove extension in file names 
```
RewriteEngine On
RewriteCond %{REQUEST_FILENAME} !-f
RewriteRule ^([^\.]+)$ $1.php [NC,L]
```

### 301 redirects
Change page URLs with [301 redirects](https://support.google.com/webmasters/answer/93633?hl=en)
```
# RewriteEngine On
# Redirect 301 /my-name-url http://new-domian.mx/my-name-url
```

### Force connection https:// for my domain
```
# Force HTTPS:// in my domian
RewriteEngine On
RewriteCond %{HTTPS} !=on
RewriteRule ^(.*)$ https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301,NE]
```

