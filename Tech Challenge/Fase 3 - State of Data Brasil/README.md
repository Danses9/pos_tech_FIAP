# Tech Challenge Fase 3 · State of Data Brasil

**Estudo de caso (PT/EN):** https://danses9.github.io/pos_tech_FIAP/state-of-data/

Pipeline de dados na AWS para analisar três edições da pesquisa State of Data Brasil (2023, 2024 e 2025, Data Hackers + Bain & Company), com 14.002 respostas, e responder 7 perguntas sobre o mercado brasileiro de Dados e IA.

## Arquitetura

```text
CSV → S3 Raw → Glue (raw_para_cleansed) → Cleansed
    → Glue (cleansed_para_transformed) → Transformed
    → Glue (transformed_para_curated) → Curated
    → Glue Crawler + Data Catalog → Athena → notebook Python
```

## Alguns resultados

- **48,3%** dos profissionais usam AWS em 2025. Em 2023 a nuvem mais citada era a Azure.
- **6,6%** das empresas não priorizam IA Generativa em 2025. Eram 20,8% em 2023.
- **R$ 18 mil** é o salário mediano de ML/AI Engineer em 2025, o maior entre os cargos.
- **22%** dos respondentes são mulheres, e a participação cai nos níveis mais altos.

## Estrutura

| Pasta | Conteúdo |
|---|---|
| `src/etl/` | Jobs PySpark do AWS Glue, um por camada |
| `src/sql/` | Consultas do Athena usadas para responder às perguntas |
| `data/outputs/` | Tabelas curadas exportadas, uma pasta por pergunta |
| `notebooks/` | Análises e gráficos em Python (pandas + matplotlib) |
| `arquitetura-tech-challenge.drawio` | Diagrama da arquitetura |

Os CSVs brutos da pesquisa não estão neste repositório. Para rodar o notebook basta `data/outputs/`.

## Tecnologias

AWS S3 · AWS Glue · PySpark · Glue Data Catalog · Amazon Athena · SQL · Parquet · Python · pandas · matplotlib

## Créditos

Projeto desenvolvido em grupo na Pós-Tech FIAP. Repositório original do grupo: https://github.com/monicajss/fiap_techchallenge/tree/master/fase-3
