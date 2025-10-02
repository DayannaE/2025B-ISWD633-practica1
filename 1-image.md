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
<img width="693" height="106" alt="imagen" src="https://github.com/user-attachments/assets/2919c813-b4c8-4b6c-98bd-e77121642ab8" />


**¿Qué es nginx**

Nginx es un servidor web que entrega contenido (como páginas web, imágenes, videos) a los usuarios a través de Internet. También puede ser un proxy inverso, lo que significa que se coloca entre los usuarios y otros servidores para redirigir o balancear el tráfico, mejorando la velocidad y confiabilidad del servicio.

Descargar la imagen  **nginx** en la versión **alpine**

<img width="668" height="220" alt="imagen" src="https://github.com/user-attachments/assets/56b45173-46ea-417c-80ab-a54d682b98ba" />


### Listar imágenes

```
docker images
```

# COLOCAR UNA CAPTURA DE PANTALLA DEL RESULTADO 
<img width="680" height="317" alt="imagen" src="https://github.com/user-attachments/assets/2027b442-c4fc-4439-ad48-c61aca6671ee" />


**Identificadores**

En Docker, se utilizan varios identificadores para diferenciar de manera única los elementos del sistema, como imágenes, contenedores, volúmenes y redes. Estos identificadores son generados automáticamente por Docker y son únicos dentro del contexto del sistema Docker en el que se encuentran. 

### Inspeccionar una imagen
El comando docker inspect se utiliza para obtener información detallada sobre un objeto de Docker específico, como un contenedor, una imagen, un volumen o una red.  Proporciona información en formato JSON sobre el objeto especificado.

```
docker inspect <nombre imagen>
docker inspect <nombre imagen>:<tag>
```

Inspeccionar la imagen hello-world 

<img width="901" height="743" alt="imagen" src="https://github.com/user-attachments/assets/7ea0c249-873a-4afe-9c63-e074fe2243cd" />


**¿Con qué algoritmo se está generando el ID de la imagen**

<img width="855" height="49" alt="imagen" src="https://github.com/user-attachments/assets/c6f841e0-2286-4710-9b3f-56f47ad17a25" />


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

<img width="679" height="72" alt="imagen" src="https://github.com/user-attachments/assets/7eb56c87-31af-4a3b-ae47-a1b64213e504" />


-f: Es la opción para forzar la eliminación de la imagen incluso si hay contenedores en ejecución que utilizan esa imagen.
Cuando eliminas una imagen Docker, Docker no elimina automáticamente los contenedores que se han creado a partir de esa imagen. Esto significa que, aunque hayas eliminado la imagen, el contenedor seguirá ejecutándose normalmente.  
**Considerar**
Eliminar una imagen no afecta a los contenedores que se han creado a partir de esa imagen, a menos que esos contenedores dependan de archivos o configuraciones específicas de la imagen eliminada. En ese caso, es posible que los contenedores se comporten de manera inesperada después de eliminar la imagen.
Es una buena práctica detener y eliminar todos los contenedores que dependan de una imagen antes de eliminar la imagen en sí.

<img width="658" height="444" alt="imagen" src="https://github.com/user-attachments/assets/c7f8b55a-667c-4774-875c-af70ad6cabed" />


```
docker rmi -f <nombre imagen>:<tag>
```
