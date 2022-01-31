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
