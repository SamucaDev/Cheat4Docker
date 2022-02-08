# Comandos mais utilizados no docker

## Listar os container que estão sendo executados

O comando **`container ls`** traz todos os containers que estão ativos.

[Link para documentação](https://docs.docker.com/engine/reference/commandline/container_ls)

### Exemplos

Exemplo #1 Listar no modelo tabela os container que estão sendo executados.

```docker
docker container ls -la

Saída:
CONTAINER ID   IMAGE     COMMAND                  CREATED          STATUS    PORTS     NAMES
762d4b84f8a6   mongo     "docker-entrypoint.s…"   28 minutes ago   Created             mongodb
```
## Entrega uma lista dos ultimos logs emitidos pelo container

O comando `docker service logs --tail=<numero-de-linhas> -f <nome-do-projeto>` traz os ultimos logs emitidos pelo projeto.

### Exemplos

Exemplo #1 lista os logs do projeto convidados
```docker
sudo docker service logs --tail =100 -f convidados

Saída:
| 2022-02-08T10:32:26.456Z [info]: ------------------------------------------------------------------
| 2022-02-08T10:32:26.456Z [info]: Projeto convidados iniciado
| 2022-02-08T10:32:26.456Z [info]: ------------------------------------------------------------------

```
