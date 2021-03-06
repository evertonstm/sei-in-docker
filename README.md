# SEI - Sistema Eletrônico de Informações usando docker

Alternativa a versão do MPOG [sei-vagrant](https://softwarepublico.gov.br/gitlab/sei/sei-vagrant/tree/master) usando docker puro e imagens já otimizadas para cada módulo.

## @TODO things

- [ ] Testar eficácia do dockerfile usando mariadb.
- [ ] Criar variável de ambiente para atualizar parâmetros de url no banco de dados para. Ex.: padronizar variáveis escritas no docker compose ou dockerfile;
- [ ] Criar variáveis de: SIGLA_ORGAO, PAGINA_INICIAL e DESCRICAO_ORGAO;
- [ ] Verificar a possibilidade de atualizar a senha do usuário root;
- [ ] Clean code na imagem do apache/php;
- [ ] Criar README.md pra imagem do apache/php;
- [ ] Verificar a possibilidade de criar variáveis de ambiente para atualizarem os arquivos de configuração do SEI/SIP através do docker-compose ou dockerfile;

## Como contribuir

O primeiro passo para contribuir é fazer um fork do repositório original em sua conta do Github. Para fazer isso, acesse o endereço [sei-in-docker](https://github.com/diogosm/sei-in-docker) e clique no botão fork(vide imagem abaixo).

![captura de tela de 2018-04-24 13-28-26](https://user-images.githubusercontent.com/1641686/39203833-fe2cfe40-47c3-11e8-8f3c-649329b492b5.png)

## Como executar

A execução pode ser individual usando cada Dockerfile ou usando docker composer

Para construir (build):

```
docker-compose build
```

Para construir cada serviço individualmente:

```
docker-compose build $SERVICE_NAME
```

Para executar (`$SERVICE_NAME` é opcional, para execução de um serviço em si)

```
docker-compose up -d $SERVICE_NAME
```

