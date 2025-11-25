# Monitoring Prometheus

Configuração simples de monitoramento utilizando **Prometheus**,
**cAdvisor**, **Node Exporter** e **Blackbox Exporter**, com
visualização via **Grafana**.

------------------------------------------------------------------------

## 🚀 Como rodar

1.  Clone o repositório:

    ``` bash
    git clone https://github.com/elder-tome/monitoring-prometheus.git
    cd monitoring-prometheus
    ```

2.  Suba os containers:

    ``` bash
    docker compose up -d
    ```

3.  Acesse o Grafana:

        http://localhost:3100

    Login padrão: **admin / admin**

------------------------------------------------------------------------

## ⚙️ Configurando o Data Source (Prometheus)

1.  No Grafana, acesse **Connections → Data sources**.

2.  Clique em **Add data source**.

3.  Escolha **Prometheus**.

4.  No campo **HTTP URL**, coloque:

        http://prometheus:9090

5.  Clique em **Save & Test**\
    Deverá aparecer a mensagem **"Data source is working"**.

------------------------------------------------------------------------

## 📊 Importando Dashboards no Grafana

1.  No menu lateral, vá para **Dashboards → Import**.
2.  Cole o ID do dashboard.

    | Serviço           | ID do Dashboard  |
    |-------------------|------------------|
    | cAdvisor          | **193**          |
    | Node Exporter     | **1860**         |
    | Blackbox Exporter | **13659**        |

3.  Quando solicitado, selecione o Data Source **Prometheus**.

------------------------------------------------------------------------

## ✔️ Pronto!

Sua stack de monitoramento estará funcionando com métricas de
**máquina**, **containers** e **checagem HTTP**.
