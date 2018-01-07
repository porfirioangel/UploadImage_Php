# Upload Image

Este proyecto es un ejemplo de backend con Php para subir imágenes 
provenientes de una app de Ionic 3.

## Instrucciones para modo desarrollador:
**Iniciar servidor:**
```
php -S 0.0.0.0:8000
```

## Instrucciones para modo producción:
1. Copiar carpeta del proyecto en ```/var/www/html```
2. Crear la carpeta ```uploads```
3. Dar los permisos correctos: ```sudo chmod -R 777 UploadImage_Php```

## Corrección de errores:
### La imagen sobrepasa límite de tamaño
#### Síntomas:

Se obtiene un log ```Received size: 0M```

#### Solución:

Abrir el archivo ```/etc/php/7.0/apache2/php.ini``` y establecer los siguientes 
parámetros: 
```
; Maximum allowed size for uploaded files.
upload_max_filesize = 40M

; Must be greater than or equal to upload_max_filesize
post_max_size = 40M
```