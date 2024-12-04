# MongoDB Atlas API for Zabbix 

## Overview
Este repositório contém um template para o Zabbix que permite o monitoramento de métricas do MongoDB Atlas através da API do MongoDB Atlas. O template foi desenvolvido para facilitar a integração entre o Zabbix e o MongoDB Atlas. Ele oferece a coleta automatizada de métricas importantes e permite a descoberta automática de nodes e métricas, facilitando a configuração e o gerenciamento de monitoramento no Zabbix. As principais funcionalidades incluem:

- Status do Cluster: Verifica a saúde geral dos clusters do MongoDB Atlas.
- Métricas de Performance: Monitora o uso de CPU, memória, e IO de discos de cada cluster.
- Métricas de Banco de Dados: Acompanha a performance de leitura e escrita, latência e utilização de conexões.
- Monitoramento de Operações e Querys: Acompanha o número de operações realizadas e o tempo de execução de queries.

## Requisitos
- Zabbix Server: Versão 6.x ou superior.
- MongoDB Atlas: Conta ativa e acesso à API do MongoDB Atlas.
- API Key: Credenciais para acessar a API do MongoDB Atlas (com permissões para leitura das métricas).
## Como Utilizar
### Configuração da API do MongoDB Atlas:

- Crie um API Key no MongoDB Atlas com as permissões necessárias para acessar as métricas do seu cluster. 

Como obter sua organizationID no MongoDB Atlas
- organizationID -> {$ORG.ID}

![organizationID](https://docs.stacktape.com/static/9a2d0c80388371e3ec580ab73c22487b/a94c1/screen5-mod.png)

Como obter API KEY MongoDB Atlas
- Public Key -> {$PUBLIC.KEY}
- Private Key -> {$PRIVATE.KEY}

![getAPIKEY](https://docs.stacktape.com/static/88a0f7162948f75898c7f3a7d8160e5a/a94c1/screen10-mod.png)


### Zabbix:

- Importe os templates em seu Zabbix.
- As informações devem ser passadas nas MACROS dentro dos dois templates.
- Crie e configure <b>um Host no Zabbix</b> com o template <i>"Mongo Atlas API - LLD Projects"</i> para descobrir os projetos criados no MongoDB Atlas, e com isso ele descobrirá e criará um host para cada projeto que houver cluster vinculado.

Após a configuração, as métricas estarão disponíveis no Zabbix para análise e alertas em tempo real.



Projeto criado por <b>Wigney Sarmento</b>, e como realizei ajustes consideráveis, resolvi fazer o fork do projeto original invés de fazer um <i>"pull requests"</i>.
