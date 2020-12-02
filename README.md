# TDCPOA 2020 - Digerindo dados com Apache NiFi

## Redes Sociais

[LinkedIn](https://www.linkedin.com/in/eliezerzarpelao/)
[Instagram](https://www.instagram.com/eliezerzarpelao/)
[Twitter](https://twitter.com/eliezerzarpelao)
[WebSite](http://eliezerzarpelao.eti.br/)

## Começando

Certifique-se de ter instalado o docker na sua máquina

[Download do Docker Desktop](https://www.docker.com/get-started)

## Desenvolvimento

Para iniciar o desenvolvimento, é necessário os passos abaixo:

clonar o projeto  num diretório de sua preferência:

```shell
cd "diretorio"
git clone --recurse-submodules https://github.com/elizarp/tdc-poa-2020-nifi.git
cd tdc-poa-2020-nifi
```

Dê uma olhada no arquivo docker-compose.yml. Se preferir pode mudar a senha que está na linha 25.

```shell
docker-compose -p proj-tdc-poa-2020-nifi up
```

## Links locais

NiFi: [http://127.0.0.1:8080/nifi](http://127.0.0.1:8080/nifi)

REDIS Insight: [http://127.0.0.1:8001](http://127.0.0.1:8001)

MongoDB Cloud (free) [https://www.mongodb.com/try](https://www.mongodb.com/try)

## Orientações Template NiFi

1. Clique em uma área branca em seguida, clique no botão de upload de template, localizado na caixa Operate, conforme imagem abaixo.

2. Efetue o upload do arquivo TemplateTDCPOA2020.xml, que está nesse repositório

3. Arraste a opção template para uma área branca do fluxo e selecione o template no combo

4. Clique com o botão direito no Process Group e em Configure para ativar (clicando no rainho) para ativar os serviços do Controller Service desse Process Group. No service do Redis você precisará colocar novamente a senha do REDIS que está no docker-compose.yml.

5. Não esqueça de acertar a configuração do e-mail e do MongoDB.

6. Inicie o fluxo, envie o arquivo people.csv para o e-mail configurado no primeiro processor e seja feliz!
