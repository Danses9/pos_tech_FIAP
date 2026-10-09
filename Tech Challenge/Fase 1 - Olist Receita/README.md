# Tech Challenge Fase 1 · Análise de Receita Olist

**Estudo de caso (PT/EN):** https://danses9.github.io/pos_tech_FIAP/olist-receita/

Análise exploratória de cerca de 100 mil pedidos do e-commerce Olist (2016 a 2018) para responder três perguntas de investidor:

- A receita está crescendo?
- Esse crescimento é estável ou volátil?
- O crescimento vem de preço ou de volume?

## Principais resultados

- **R$ 15,8 milhões** de receita (produto + frete) em **99.441 pedidos**.
- **+139%** de receita de janeiro a agosto de 2018 em relação ao mesmo período de 2017.
- Depois do pico da Black Friday de 2017, a receita se manteve acima de **R$ 1 milhão** em 7 dos 8 meses de 2018.
- **Correlação de 0,996** entre pedidos e receita no mês, com ticket médio estável (R$ 145 a R$ 172): o crescimento vem do volume.
- **73%** da receita vem de 5 estados, com São Paulo respondendo por 37%.

## Conteúdo

| Arquivo | O que é |
|---|---|
| `exploracao_tech.ipynb` | Notebook com preparação, métricas, testes estatísticos e gráficos |
| `graficos/` | Gráficos finais usados no relatório |

## Como executar

Baixe o [Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) e ajuste a variável `path` no notebook para a pasta onde estão os CSVs. Os arquivos usados são `olist_orders_dataset.csv`, `olist_order_items_dataset.csv` e `olist_customers_dataset.csv`.

## Tecnologias

Python · pandas · NumPy · SciPy · matplotlib · seaborn

## Créditos

Projeto em grupo na Pós-Tech FIAP. Esta pasta reúne a minha parte, a análise de receita. Repositório do grupo: https://github.com/monicajss/fiap_techchallenge/tree/master/fase-1
