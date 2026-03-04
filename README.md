# 🚀 n8n + Evolution API Stack

Este repositório contém a infraestrutura como código (usando Docker Compose) para provisionar rapidamente um ambiente completo de automação de fluxos e mensageria.

O ambiente é orquestrado para subir instâncias locais do n8n, Evolution API (para integrações de WhatsApp), além dos bancos de dados necessários para suportar a operação.

## 🛠️ Tecnologias e Arquitetura

A stack é composta pelos seguintes serviços

 [n8n](httpsn8n.io) Plataforma de automação de fluxos de trabalho baseada em nós.
 [Evolution API](httpsevolution-api.com) API RESTful para integração e gestão de instâncias do WhatsApp.
 [PostgreSQL](httpswww.postgresql.org) Banco de dados relacional (base para futuras integrações com Supabase e armazenamento da Evolution API).
 [Redis](httpsredis.io) Banco de dados em memória utilizado para gerenciamento de filas e cache da Evolution API.

## ⚙️ Pré-requisitos

Antes de começar, você precisará ter as seguintes ferramentas instaladas na sua máquina

 [Docker](httpsdocs.docker.comget-docker)
 [Docker Compose](httpsdocs.docker.comcomposeinstall)
 [Git](httpsgit-scm.com)

## 🚀 Como executar o projeto

1. Clone este repositório
   ```bash
   git clone [git@github.com:jadsonmorais/omnichannel-automation-env.git](git@github.com:jadsonmorais/omnichannel-automation-env.git)
   cd omnichannel-automation-env

   Suba os containers em segundo plano:
    Bash

    docker compose up -d

    Para visualizar os logs e acompanhar a inicialização:
    Bash

    docker compose logs -f

    Para parar e remover os containers:
    Bash

    docker compose down

🌐 Acessos Locais

Assim que os serviços estiverem rodando, eles estarão disponíveis nos seguintes endereços:

    n8n: http://localhost:5678

    Evolution API: http://localhost:8080

    PostgreSQL: localhost:5432

    Redis: localhost:6379

🔒 Notas de Segurança

    As credenciais (senhas e chaves de API) no docker-compose.yml atual estão configuradas para um ambiente de desenvolvimento/teste.

    Antes de levar essa infraestrutura para produção, é mandatório substituir as variáveis de ambiente por senhas fortes e, preferencialmente, utilizar um arquivo .env para não expor credenciais no repositório.


***

**Gostaria que eu te enviasse também um arquivo `.gitignore` padrão para esse tipo de projeto Docker, garantindo que você não suba arquivos temporários do VS Code para o seu GitHub sem querer?**