# Tech Challange 01 - NPS Preditivo

## Objetivo

Entender, dado o problema de negócio, os fatores operacionais que influenciam o NPS permitindo a tomada de decisões estratégicas de forma a aumentar a satisfação do cliente, assim como predizer e tomar decisões em tempos real que permitam ações proativas que aumentem a satisfação do cliente.

## Base de Dados

A base de dados contém 19 variáveis, com 2500 linhas de dados, todos únicos, sem valores nulos e sem valores fora dos limites esperados (por exemplo, não há nota de NPS negativas).

| # | Variável | Tipo (pandas) | Natureza | Descrição |
|---|----------|--------------|----------|-----------|
| 0 | `customer_id` | int64 | Categórica | Identificador único do cliente |
| 1 | `customer_age` | int64 | Numérica | Idade do cliente |
| 2 | `customer_region` | object | Categórica | Região geográfica do cliente |
| 3 | `customer_tenure_months` | int64 | Numérica | Tempo de relacionamento com a empresa (meses) |
| 4 | `order_id` | int64 | Categórica | Identificador único do pedido |
| 5 | `order_value` | float64 | Numérica | Valor total do pedido (R$) |
| 6 | `items_quantity` | int64 | Numérica | Quantidade de itens no pedido |
| 7 | `discount_value` | float64 | Numérica | Valor de desconto aplicado ao pedido (R$) |
| 8 | `payment_installments` | int64 | Numérica | Número de parcelas do pagamento |
| 9 | `delivery_time_days` | int64 | Numérica | Tempo total de entrega (dias) |
| 10 | `delivery_delay_days` | int64 | Numérica | Dias de atraso na entrega |
| 11 | `freight_value` | float64 | Numérica | Valor do frete (R$) |
| 12 | `delivery_attempts` | int64 | Numérica | Número de tentativas de entrega |
| 13 | `customer_service_contacts` | int64 | Numérica | Número de contatos do cliente com atendimento |
| 14 | `resolution_time_days` | int64 | Numérica | Tempo para resolução de problemas (dias) |
| 15 | `nps_score` | float64 | **🎯 Target** | Nota de satisfação NPS (0–10), coletada após a compra |
| 16 | `repeat_purchase_30d` | int64 | Categórica | Recompra em até 30 dias (0 = não, 1 = sim) |
| 17 | `complaints_count` | int64 | Numérica | Número de reclamações registradas pelo cliente |
| 18 | `csat_internal_score` | float64 | Numérica | Score interno de satisfação do cliente |

## Metodologia

A metodologia utilizada baseia-se no CRISP-DM. Seguiram-se as seguintes fases:

1. Entendimento de negócio: Buscou-se entender o NPS, como é importante na área de e-commerce e como está contextualizado no problema em questão. Através dessa fase definiu-se a pergunta que irá nortear as fases seguintes. 
2. Entendimento dos dados: Buscou-se entender os dados em si, começando pela validação da qualidade, verificando se havia valores discrepantes, nulos ou duplicados. Por fim, analisou-se os dados de uma visão de estatistica descritiva, após isso aprofundou-se nos dados procurando entender as correlações existentes.
3. Preparação dos dados: Realizou-se a preparação dos dados para o problema, em especial com a criação de classes do NPS, criando-se uma coluna para classificar em detrator, neutro e promotor. 

## Reprodução dos Resultados

Requerimentos:
```
git
python3
jupyterlab # para o notebook interativo
```

### Passo a Passo
Clone o repositório:
```sh
git clone https://github.com/jcdematos/fiap-iast-tech-challange-01.git
```

Instale as bibliotecas utilizadas:
```sh
pip install -r requirements.txt
```

Execute o EDA:
```sh
python3 reports/EDA.py
```

> Os dados serão carregados do repositório público, e não precisam ser baixados localmente. 

Também pode-se executar o notebook interativo disponível em `notebooks/`
