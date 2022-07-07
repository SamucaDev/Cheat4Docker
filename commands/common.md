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

## Criar secrets para serem utilizadas nas aplicações

Entre na pasta que seja criar os arquivos de secret.

Crie o arquivo:

```cmd
sudo touch <secret>.json
```

agora devemos inserir o conteúdo nesta secret criada.

```cmd
sudo nano <secret>.json
```

Abriu o editor de texto nano, devemos incluir o conteúdo da secret, como trata-se de um arquivo json devemos escrever um objeto de chave e valor.

```JSON
{
  "EXEMPLE_LOGIN": "XXXX.XXXX",
  "EXEMPLE_PASSWORD": "YYYYY",
}
```

Arquivo criado porém precisamos rodar um comando docker para registrar as secrets em no contexto docker, para isso: 

```docker 
sudo docker secret create <secret> <secret>.json
```

Saída: XPTOXPTOXPTODJDSADJAS -> Id unico da sua secret para o docker
```docker
2022-02-08T10:32:26.456Z [info]: XPTOXPTOXPTODJDSADJAS
```

## Como verificar as imagens que temos na máquina

```
docker image list
```
