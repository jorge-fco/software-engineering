# Server
- **Domian:**
- **Hosting:**
- **DNS:**
- **MX Records:**

**CNAME:**
Registro CNAME es un tipo de registro DNS que asigna un alias a un nombre de dominio auténtico o canónico. Los registros CNAME se suelen utilizar para asignar un subdominio, como www o mail, al dominio que aloja el contenido de dicho subdominio.

Por ejemplo, un registro CNAME puede asignar la dirección web www.example.com al sitio web real del dominio example.com.

**SMTP:**
(_Simple Mail Transfer Protocol_) es un protocolo de red utilizado para el intercambio de mensajes de correo electrónico entre computadoras u otros dispositivos.

**.htaccess:** _Hypertext Access_. Archivo de configuración para servidores web basados en Apache.

- Change page URLs with [301 redirects](https://support.google.com/webmasters/answer/93633?hl=en)

```
# RewriteEngine On
# Redirect 301 /my-name-url http://new-domian.mx/my-name-url
```

```
# Force HTTPS:// in my domian
RewriteEngine On
RewriteCond %{HTTPS} !=on
RewriteRule ^(.*)$ https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301,NE]
```

### LocalHost server
1.- Acceder al directorio de host.
```
sudo nano /private/etc/hosts
```

2.- Password de mi PC.
```
enter password:
```

3.- IP
```
00.27.46.200 mydomian.com www.mydomian.com
```

4.- Comentar lineas de código # (gato + espacio)
```
# example host
# 00.27.46.200 mydomian.com www.mydomian.com
```

5.- `ctrl` + `o` + `ENTER` para guadar.

6.- `ctrl` + `x` para salir del host files.

7.- Realizar flush al cache.
```
dscacheutil -flushcache
```
