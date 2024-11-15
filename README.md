# MongoDB Atlas API for Zabbix 

## Overview
Este repositório contém um template para o Zabbix que permite o monitoramento de métricas do MongoDB Atlas através da API do MongoDB Atlas. O template foi desenvolvido para facilitar a integração entre o Zabbix e o MongoDB Atlas. Ele oferece a coleta automatizada de métricas importantes e permite a descoberta automática de nodes e métricas, facilitando a configuração e o gerenciamento de monitoramento no Zabbix. As principais funcionalidades incluem:

- Status do Cluster: Verifica a saúde geral dos clusters do MongoDB Atlas.
- Métricas de Performance: Monitora o uso de CPU, memória, e IO de discos de cada cluster.
- Métricas de Banco de Dados: Acompanha a performance de leitura e escrita, latência e utilização de conexões.
- Monitoramento de Operações e Querys: Acompanha o número de operações realizadas e o tempo de execução de queries.

## Requisitos
- Zabbix Server: Versão 5.x ou superior.
- MongoDB Atlas: Conta ativa e acesso à API do MongoDB Atlas.
- API Key: Credenciais para acessar a API do MongoDB Atlas (com permissões para leitura das métricas).
## Como Utilizar
### Configuração da API do MongoDB Atlas:

- Crie um API Key no MongoDB Atlas com as permissões necessárias para acessar as métricas do seu cluster.
- Importação no Zabbix:

- Importe o template no seu servidor Zabbix.
- Configure um Host no Zabbix para o MongoDB Atlas, utilizando as credenciais da API e o URL do MongoDB Atlas.

Após a configuração, as métricas estarão disponíveis no Zabbix para análise e alertas em tempo real.
Personalização
Este template pode ser facilmente estendido ou modificado para atender a necessidades específicas de monitoramento do MongoDB Atlas. As chaves e triggers podem ser ajustadas para coletar informações adicionais ou para configurar alertas personalizados.


Como obter sua organizationID no MongoDB Atlas
- organizationID -> {$KEY_CLUSTER}

![organizationID](https://docs.stacktape.com/static/9a2d0c80388371e3ec580ab73c22487b/a94c1/screen5-mod.png)

Como obter API KEY MongoDB Atlas
- Public Key -> {$USER_KEY}
- Private Key -> {$PASS_KEY}

![getAPIKEY](https://docs.stacktape.com/static/88a0f7162948f75898c7f3a7d8160e5a/a94c1/screen10-mod.png)
