# Docker.Services
This is simple docker-compose file that runs the latest version of:
    -Cassandra 4.0,
    -Consul 1.11
    -Elders/RabbitMq (3.9.11)
    
    

# Usage
    

docker-compose.yml can be run in a local environment by going into the root directory of each one and executing:

```
$ docker-compose up

```

    
    
    
# Expected result
    
    
    
Listing containers must show three containers running and the port mapping as below:
    
```
CONTAINER ID   IMAGE                       COMMAND                  CREATED          STATUS          PORTS
22cec4515da0   cassandra:4.0               "docker-entrypoint.s…"   25 minutes ago   Up 25 minutes   7000-7001/tcp, 7199/tcp, 9160/tcp, 0.0.0.0:9042->9042/tcp 
5fdafc3581a4   eldersoss/rabbitmq:3.9.11   "docker-entrypoint.s…"   25 minutes ago   Up 25 minutes   4369/tcp, 5671/tcp, 0.0.0.0:5672->5672/tcp, 15671/tcp, 15691-15692/tcp, 25672/tcp
51c4cfa5fe08   consul:1.11                 "docker-entrypoint.s…"   25 minutes ago   Up 25 minutes   0.0.0.0:8300-8302->8300-8302/tcp, 0.0.0.0:8400->8400/tcp

```
    
    
    
# Stop and remove the containers 

```
$ docker-compose down

```
