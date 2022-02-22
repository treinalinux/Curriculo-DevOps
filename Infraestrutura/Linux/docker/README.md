# Docker

## Comandos

```
# docker container run hello-world
# docker image ls
# docker ps
# docker container ls
# docker container ls -a
# docker container run -ti centos:7
# docker container run -ti ubuntu
# docker container -d nginx
# docker container attach [CONTAINER ID]
# docker container exec -ti [CONTAINER ID] [COMANDO]
# docker container start [CONTAINER ID]
# docker container stop [CONTAINER ID]
# docker container restart [CONTAINER ID]
# docker container pause [CONTAINER ID]
# docker container unpause [CONTAINER ID]
# docker container start [CONTAINER ID]
# docker container stop [CONTAINER ID]
# docker container restart [CONTAINER ID]
# docker container pause [CONTAINER ID]
# docker container unpause [CONTAINER ID]
# docker container inspect [CONTAINER ID]
# docker container logs -f [CONTAINER ID]
# docker container rm [CONTAINER ID]
# docker container attach [CONTAINER ID]
# docker container rm -f [CONTAINER ID]
# docker container exec -ti [CONTAINER ID] [COMANDO]
# docker container run -d nginx
# docker container stats [CONTAINER ID]
# docker container top [CONTAINER ID]
# docker container run -d -m 128M --cpus 0.5 nginx
# docker container update --memory 64M --cpus 0.4 nginx
# docker container inspect [CONTAINER ID]
# docker container stats [CONTAINER ID]
# docker container top [CONTAINER ID]

Comando executados dentro do container:

# apt-get update
# apt-get install stress
# stress --cpu 1 --vm-bytes 128M --vm1
```

### Na prática

```
docker container run -ti ubuntu

docker start 82ea85c77bec

# Nesse caso é possível atachar ao container, o principal processo é o bash.
docker container attach 82ea85c77bec
```


```
# Aqui você não executado o -it, pois o principal processo é o próprio nginx
# o -d executa como segundo plano
docker container run -d nginx

# Não é possível atachar, mas se quiser acessar o container, use o -it container-id bash
docker container exec -it 11368337a93c bash
```


```
# IP interno do container 

docker container inspect eb10aace9b58 | grep 172

# Logs 
docker container logs -f eb10aace9b58

# testando o IP do container
curl 172.17.0.2

```


```

```
