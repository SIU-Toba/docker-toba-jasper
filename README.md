# docker-toba-jasper
Contenedor Docker para iniciar Jasper 

## Requerimientos
 * Se debe tener instalado [Docker](https://docs.docker.com/installation/)

## Build
```
docker build -t="siutoba/docker-toba-jasper" .
```
Una vez hecho el push a github automáticamente se va a actualizar la imagen en el índice de [hub.docker.com](hub.docker.com)

## Configuración docker-compose.yml
```
jasper:
  image: siutoba/docker-toba-jasper
  container_name: proyecto-jasper-uv
  ports:
   - "8081:8081"
  links:
   - pg
  volumes:
   - ./vendor/siu-toba/jasper:/var/local/jasper
   - ./:/var/local/proyecto
```
