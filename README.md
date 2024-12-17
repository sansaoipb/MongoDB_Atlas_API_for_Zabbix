# Doações
<table>
    <tr>
        <td> <!-- PagSeguro -->
            <h3>
                <div align="center">PagSeguro</div>
            </h3>
            <a href="https://pag.ae/7_b_5Kn-t">
            <img src="https://stc.pagseguro.uol.com.br/public/img/botoes/doacoes/120x53-doar.gif"></a>
        </td>
        <td> <!-- PayPal -->
            <h3>
                <div align="center">PayPal</div>
            </h3>
            <a href="https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=7VVS675TLJHUL&lc=BR&item_name=Eracydes%20Lima%20Carvalho%20Junior&currency_code=BRL&bn=PP%2dDonationsBF%3abtn_donateCC_LG%2egif%3aNonHosted">
            <img src="https://www.paypalobjects.com/pt_BR/BR/i/btn/btn_donateCC_LG.gif"></a>
        </td>
        <td> <!-- PicPay -->
            <h3>
                <div align="center">PicPay</div>
	        </h3>
            <a href="https://picpay.me/sansaoipb">
            <img src="https://lh3.googleusercontent.com/PX1pBd24_ygdLwvKMFrnUhJqGzG-YmhbYPkE8FM74qdXc-na7EqIA808F-7WAjZnvjziEESYZz2n8Ofn6WGdTrRufae_A7WbEVA5xASAUDpWNyqcVKE0GKNJrEVMBLCee5evEdrgJn8PgaI0E7qr0QDf6lTuCHI9osuziJwJ8-OTiR1JMOWLPLrw-wOW7IZ3DQCkyQECZpb_123x1K1fKNRw6cIyEWSgYRVwzX3PeljmxyH-EBOF-1wrO67-4rLP0CfbpRxJaX3pMyNlFZMLD0R6k6HvL1ax328z0qLafMwHjLPFlVEcyMkl-CFwJN9vgP37plpZ76NNruCBkj6W-MKQkvLevjcjf-Zq718N7ow8ZSlvUOCCZFJ1ieZZrLOINaMsmYGqMYpGEMME910zzAKtd-dm0IJ0TQTx_pZ0BXniK0HCvVhNHhPiYNYJGBMv_wlakLQ8XIcBdi0iIaEOFvrGSHhXEbDx6OZ9EKsvXQNoKBRwXD0Nnqxf3o-HW0U-P3pAskj3GSBa9qfvQqK-P4pxG98hYJ4st7_FA655I9n5bP-E6lIgFqvdJC8odyVfXFpHtVWfaO9_WVXowqdiXKzX9qQ9PetQNhTnJG_WgoqocmIh1FJhAYd08fonFfbmS_Hhnvi5qqxQytCqYxqWfh1elL18X8c=w120-h53-no"></a>
        </td>
    </tr>
</table>

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
