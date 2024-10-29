# COMPLETAR  
Comparando sus conocimientos antes de hacer la práctica con sus conocimientos después de hacer la tarea, explicar los principales aprendizajes logrados para beneficio de su formación profesional.  
Si solucionó un problema presentado o utilizó otros comandos que no se mencionan al realizar la práctica también se debe documentar.
***

Antes de realizar esta práctica, mi conocimiento sobre Docker era aceptable en la creación de contenedores y su ejecución en un entorno simple. Mi comprensión se centraba en los conceptos de imágenes, contenedores y redes sin un entendimiento claro sobre volúmenes y la configuración avanzada que puede involucrar Docker, especialmente cuando se usa para aplicaciones complejas como Drupal.

En que aspectos me ayudo esta práctica, los detallo a continuación:

#### 1. Uso y manejo de Volumenes
Un aspecto crucial en esta práctica fue aprender a crear y montar volúmenes persistentes (como vol-drupal-files, vol-drupal-modules, vol-drupal-profiles y vol-drupal-sites). Antes de esta práctica, no comprendía la importancia de los volúmenes para la persistencia de datos, pero ahora entiendo cómo los volúmenes pueden garantizar que los datos permanezcan intactos incluso si el contenedor se detiene o se elimina.

#### 2. Configuración avanzada de contenedores y resolución de problemas
En el proceso de instalación de Drupal, me encontré con problemas de permisos y configuración de directorios específicos, como el error relacionado con el directorio de translations. Aprendí a diagnosticar y solucionar estos problemas mediante el ajuste de permisos y la creación de carpetas necesarias directamente dentro del contenedor usando comandos como docker exec para realizar cambios específicos.

#### 3. Uso de comandos adicionales
Durante la práctica, utilicé comandos adicionales como docker volume inspect para verificar los puntos de montaje de los volúmenes y docker exec para acceder al contenedor y ajustar los permisos de archivos y directorios.

### Documentación de soluciones y comandos adicionales utilizados

Resolución del problema del directorio de translations: Al encontrar el error relacionado con los permisos de este directorio, utilicé los comandos:


```
docker exec server-drupal mkdir -p /var/www/html/sites/default/files/translations

docker exec server-drupal chmod -R 775 /var/www/html/sites/default/files/translations

docker exec server-drupal chown -R www-data:www-data /var/www/html/sites/default/files
```

Estos comandos me permitieron crear el directorio y ajustar los permisos necesarios para que Drupal pudiera continuar con la instalación.
***

Autor: Kevin Asimbaya  
Fecha: 28/10/2024
***
