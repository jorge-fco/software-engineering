# Windows.

1.-
```
C:\Windows\System32\drivers\etc\hosts
```

2.-
```
127.0.0.1 www.misitio.com
```

3.- Realizar flush al cache.
```
ipconfig / flushdns
```

# MAC.
1.- Acceder al directorio de host mediante la terminal.
```
sudo nano /private/etc/hosts
```

2.- Ingresar la password de la PC.
```
enter password:
```

3.- Configurar la IP para el dominio.
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
