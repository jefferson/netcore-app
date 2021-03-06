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

A configura��o de uma aplica��o � tudo o que � prov�vel variar entre deploys (homologa��o, produ��o, ambientes de desenvolvimento, etc). 
Isto inclui:

- Recursos para a base de dados, Memcached, e outros servi�os de apoio
- Credenciais para servi�os externos como Amazon S3 ou Twitter
- Valores por deploy como o nome can�nico do host para o deploy.

Nesta aplica��o os arquivos de configura��o ser�o salvos separadamente em outro reposit�rio e ser� tratado como
subm�dulo, atrav�s do git, para que cada arquivo de configura��o possa ser versionada separadamente em cada ambiente como uma solu��o simples.

Observer que dentro do arquivo [Library.Api.csproj](./Library.Api.csproj) h� uma TargetGroup descrevendo a diretativa de inserva��o do arquivo de configura��o no ambiente de desenvolvimento.

Os arquivos de configura��o ser�o segregados por ambiente e disponibilizados na pasta ```configmap```.

Os ambientes ser�o os seguintes:
- local: m�quina do desenvolvedor
- dev: servidor de desenvolvimento
- hml: servidor de homologa��o
- prd: servidor de produ��o

Permitindo que no momento da instala��o cada aplica��o possa baixar o seu arquivo de configura��o separadamente. Os eventos descritos no arquivos de configura��o acima s�o os seguintes:

id| Evento | descricao
--| -------|----------
1 | Build  | Remover arquivo de configura��o atual
2 | Build  | Copiar arquivo local de desenvolvimento para o diret�rio da aplica��o

[Click here to visit configmap](https://github.com/jefferson/netcore-configmap)

[Click here for read more about section Configuration on 12factor.](https://12factor.net/pt_br/config)