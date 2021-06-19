# chat-docker
> TP2 - Software Libre - 2021 - FI-UNMdP

Implementación del TP de Sistemas Distribuidos (sistema de chat en Node y ZeroMQ) con Docker.

## Alumnos 
  - Mariquena Gros
  - Pablo Porzio


## Instalación

1 - Clonar repo:

```
git clone https://github.com/mariquena/chat-docker.git
```

2 - Colocarse en el directorio de trabajo:

```
cd chat-docker/project
```

3 - Instalar contenedores:

```
docker-compose up -d
```

3 - Instalar dependencias del cliente:

```
cd cliente 
npm install
```

## Ejecución de contenedores

1 - Correr: 

```
docker-compose start
```

2 - Detener: 

```
docker-compose stop
```

## Ejecución de cliente

1 - Correr: 

```
cd src
node cliente.js nombre_cliente
```

## Comandos del cliente

- Mostrar usuarios
```
showusers
```
- Crear/unirse a un grupo `nombre_grupo`
```
group nombre_grupo
```
- Escribir mensaje a `otro_usuario`
```
write otro_usuario
```
- Escribir mensaje a todos 
```
writeall
```
- Escribir mensaje en `nombre_grupo`
```
write nombre_grupo
```
- Desconectarse
```
bye
```

## Configuración adicional para Windows 

Para que funcione el sistema en Windows hay que modificar el archivo `hosts` ubicado en `Windows/system32/drivers/etc`. Para poder editarlo hay que abrir el block de notas como admin. Hay que agregar estas líneas al archivos:

```
# Chat docker
127.0.0.1	broker-1
127.0.0.1	broker-2
127.0.0.1	broker-3
127.0.0.1	coordinador
127.0.0.1	servidor-http
127.0.0.1	servidor-ntp
```

## Fuentes

- [Cómo construir arquitectura de microservicios con Node y Docker](https://www.ais.com/using-docker-compose-to-locally-develop-and-test-microservices/)
- [Imagen oficial de Node para Docker](https://hub.docker.com/_/node?tab=description&page=1&ordering=last_updated)
- [Parámetros para el archivo compose](https://docs.docker.com/compose/compose-file/compose-file-v3/)
- [Repositorio original del TP de SSDD](https://github.com/porziopablo/tp_ssdd)

