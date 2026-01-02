

📊 Pipeline de Engenharia de Dados com Databricks (ETL)


## 📌 Visão Geral

Este projeto entrega uma solução completa de Engenharia de Dados, utilizando Databricks e arquitetura Medallion (Bronze, Silver e Gold) para garantir governança, qualidade e escalabilidade dos dados.

Principais entregas:
- Extração, organização e ingestão de dados
- Limpeza, padronização e enriquecimento
- Modelagem analítica e dimensional
- Implementação em Python (PySpark) e SQL
- Adoção de boas práticas de Engenharia de Dados

O versionamento é realizado via GitHub, com integração direta ao ambiente Databricks.


## 🧠 Objetivo

O objetivo é entregar um pipeline robusto, onde os dados percorrem múltiplas camadas até estarem prontos para consumo analítico, seguindo padrões de mercado e requisitos de governança.

Competências demonstradas:
- ETL / ELT
- Databricks
- Spark
- SQL Analítico
- Organização de pipelines
- Data Warehouse



## 🛠️ Tecnologias Utilizadas

- Databricks
- Apache Spark (PySpark)
- SQL (Spark SQL)
- Git & GitHub
- Arquitetura Medallion (Bronze / Silver / Gold)


## 🗂️ Arquitetura do Projeto (Medallion)

### 🥉 Camada Bronze (Raw Data)
Armazena dados brutos, conforme ingeridos, com mínima transformação. Foco em integridade e rastreabilidade.

**Características:**
- Dados crus
- Sem regras de negócio
- Estruturação inicial

**Exemplos de tabelas:**
- album_bronze
- track_bronze

### 🥈 Camada Silver (Cleaned Data)
Responsável por limpeza, padronização e organização dos dados, aplicando regras de negócio e separação lógica de entidades.

**Transformações realizadas:**
- Remoção de colunas desnecessárias
- Padronização de nomes
- Conversão de tipos
- Tratamento de nulos
- Separação de entidades

**Exemplos de tabelas:**
- album_silver
- track_silver

### 🥇 Camada Gold (Analytics)
Contém dados prontos para consumo analítico, com modelagem dimensional e agregações para BI.

**Exemplo:**
- fact_tracks

Permite análises como:
- Quantidade de faixas por álbum
- Duração total por álbum
- Métricas agregadas para BI


## 🧱 Modelagem de Dados

Utiliza conceitos de Data Warehouse, com tabelas dimensão (ex: álbum) e tabela fato (faixas/métricas), facilitando consultas analíticas, escalabilidade e integração futura com ferramentas de BI.


## 🔄 Pipeline ETL

1️⃣ **Extração**
- Ingestão de dados no Databricks
- Armazenamento inicial na camada Bronze

2️⃣ **Transformação**
- Limpeza e padronização na camada Silver
- Aplicação de regras de negócio

3️⃣ **Carga**
- Criação de tabelas analíticas na camada Gold

Processo implementado com PySpark e Spark SQL.


## 🧪 Consultas e Análises

Consultas SQL na camada Gold para validação, análise de métricas e garantia de consistência entre tabelas, atendendo demandas reais de times de negócio e BI.


## 📁 Organização do Repositório

```text
├── bronze/
│   └── ingestao_dados.py
├── silver/
│   └── transformacoes.py
├── gold/
│   └── modelagem_fato.sql
├── consultas/
│   └── analises.sql
└── README.md
```