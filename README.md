# RabbitMQ-CSharp
## _Demo para probar las colas en RabbitMQ_

Consiste en una aplicación web que genera mensajes de diferentes colas en RabbitMQ, 
y una aplicación de consola se encarga de recibir los mensajes y sacarlos de la cola.

## Instalación

- Instalar RabbitMQ en Docker
```sh
docker pull rabbitmq

docker run -d -v rabbitmq-vol:/var/lib/rabbitmq --hostname jb-rabbit -p 5672:5672 -p 8081:15672 --name jb-rabbit rabbitmq:3-management
``` 

- Levantar una instancia de la aplicación de consola ConsumidorDEMO para la cola1
```sh
dotnet run cola1
```

- Levantar una instancia de la aplicación de consola ConsumidorDEMO para la cola2
```sh
dotnet run cola2
```

- Levantar la aplicación ProductoMQ
- Generar mensajes a las colas 1 y 2
