# Introducion

This is a App for demonstrate and apply best practices and patterns in software development.
These principes can apply in any project in any language of development.

- 12 factors app
- Clean Arachiteture
- Open Api
- Cloud computer
- Microsservices
- Docker

## Scope

## Unit Test

## How to run

## Configuration

A configuração de uma aplicação é tudo o que é provável variar entre deploys (homologação, produção, ambientes de desenvolvimento, etc). 
Isto inclui:

- Recursos para a base de dados, Memcached, e outros serviços de apoio
- Credenciais para serviços externos como Amazon S3 ou Twitter
- Valores por deploy como o nome canônico do host para o deploy.

Nesta aplicação os arquivos de configuração serão salvos separadamente em outro repositório e será tratado como
submódulo, através do git, para que cada arquivo de configuração possa ser versionamento separadamente em cada ambiente como uma solução simples.

Observer que dentro do arquivo `[Library.Api.csproj](./Library.Api.csproj)` há uma TargetGroup descrevendo a diretativa de inservação do arquivo de configuração no ambiente de desenvolvimento.

Permitindo que no momento da instalação cada aplicação possa baixar o seu módulo separadamente.

[Click here to visit configmap](https://github.com/jefferson/netcore-configmap)

[Click here for read more about section Configuration on 12factor.](https://12factor.net/pt_br/config)