# Imagen
### Descargar imagen
Descarga la última versión de la imagen disponible en el registro de Docker.

```
docker pull <nombre imagen>
```

Descarga una versión específica de la imagen, cada imagen tiene etiquetas (tags) para diferentes versiones.
Una imagen puede tener la etiqueta latest para representar la última versión, si no se especifica una etiqueta se hará referencia a la versión latest.

```
docker pull <nombre imagen>:<tag>
```

Descargar la imagen **hello-world**
```
docker pull hello-world
```

<img width="959" height="201" alt="imagen" src="https://github.com/user-attachments/assets/d5035887-bd8c-4368-8e31-ea4666aacaaa" />



**¿Qué es nginx**

Nginx es un servidor web que entrega contenido (como páginas web, imágenes, videos) a los usuarios a través de Internet. También puede ser un proxy inverso, lo que significa que se coloca entre los usuarios y otros servidores para redirigir o balancear el tráfico, mejorando la velocidad y confiabilidad del servicio.

Descargar la imagen  **nginx** en la versión **alpine**
```
docker pull nginx:alpine
```

<img width="944" height="342" alt="imagen" src="https://github.com/user-attachments/assets/4c1b0c37-a058-4fdd-b640-bfd5760bff96" />

### Listar imágenes

```
docker images
```
<img width="750" height="113" alt="imagen" src="https://github.com/user-attachments/assets/eaf664ea-edc0-4dff-9f72-34de74b1b2e0" />

**Identificadores**

En Docker, se utilizan varios identificadores para diferenciar de manera única los elementos del sistema, como imágenes, contenedores, volúmenes y redes. Estos identificadores son generados automáticamente por Docker y son únicos dentro del contexto del sistema Docker en el que se encuentran. 

### Inspeccionar una imagen
El comando docker inspect se utiliza para obtener información detallada sobre un objeto de Docker específico, como un contenedor, una imagen, un volumen o una red.  Proporciona información en formato JSON sobre el objeto especificado.

```
docker inspect <nombre imagen>
docker inspect <nombre imagen>:<tag>
```

Inspeccionar la imagen hello-world 

```
docker inspect hello-world
```

<img width="1206" height="887" alt="imagen" src="https://github.com/user-attachments/assets/f316664f-37d2-40ab-9dd0-0137965cdffa" />


**¿Con qué algoritmo se está generando el ID de la imagen**

 "sha256:54e66cc1dd1fcb1c3c58bd8017914dbed8701e2d8c74d9262e26bd9cc1642d31"

### Filtrar imágenes

```
docker images | grep <termino a buscar>

```
<img width="488" height="62" alt="imagen" src="https://github.com/user-attachments/assets/721dcae0-074d-46c4-9bfd-10152959e284" />

### Para eliminar una imagen
Eliminar permanentemente la imagen de tu sistema Docker.

```
docker rmi <nombre imagen>:<tag>
```

Eliminar la imagen hello-world 

```
docker rmi hello-world:latest
```
<img width="940" height="107" alt="imagen" src="https://github.com/user-attachments/assets/9fe79265-54ec-40db-9168-c457d743dbd2" />


-f: Es la opción para forzar la eliminación de la imagen incluso si hay contenedores en ejecución que utilizan esa imagen.
Cuando eliminas una imagen Docker, Docker no elimina automáticamente los contenedores que se han creado a partir de esa imagen. Esto significa que, aunque hayas eliminado la imagen, el contenedor seguirá ejecutándose normalmente.  
**Considerar**
Eliminar una imagen no afecta a los contenedores que se han creado a partir de esa imagen, a menos que esos contenedores dependan de archivos o configuraciones específicas de la imagen eliminada. En ese caso, es posible que los contenedores se comporten de manera inesperada después de eliminar la imagen.
Es una buena práctica detener y eliminar todos los contenedores que dependan de una imagen antes de eliminar la imagen en sí.

```
docker rmi -f <nombre imagen>:<tag>
```
