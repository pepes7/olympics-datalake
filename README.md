# Data Lake - Jogos Olímpicos

## Descrição do Projeto

Este projeto tem como objetivo a construção de um **Data Lake local** utilizando dados dos Jogos Olímpicos, organizados em diferentes camadas (**RAW, BRONZE e GOLD**), seguindo boas práticas de engenharia de dados.

O Data Lake permite armazenar, processar e analisar dados de forma estruturada, possibilitando a geração de insights a partir de diferentes fontes.

---

## Estrutura do Projeto

```
data-lake-olimpiadas/
├── raw/
├── bronze/
├── gold/
│   ├── analise_medalhas/
│   ├── analise_modalidades/
│   └── analise_genero/
├── metadata_schema.json
└── README.md
```

---

## Camada RAW (Dados Brutos)

* Contém os arquivos originais em formato **CSV**
* Cada dataset possui um arquivo **.json de metadados**

### Exemplos:

* athlete_bio.csv
* athlete_results.csv
* games.csv
* paris_athletes.csv
* paris_medals.csv
* paris_events.csv

### Metadados incluem:

* Nome do dataset
* Fonte
* Descrição
* Campos principais
* Data de coleta
* Observações

---

## Camada BRONZE (Dados Tratados)

* Conversão dos dados para formato **Parquet**
* Limpeza e normalização dos dados
* Integração entre datasets (JOINs)
* Metadados gerados automaticamente

### Contém:

* Arquivos `.parquet`
* Arquivos `.json` com metadados

---

## Camada GOLD (Dados Analíticos)

Camada responsável por análises e geração de insights.

###  Análises desenvolvidas:

####  Análise de Medalhas

* Contagem de medalhas por país

####  Análise de Modalidades

* Quantidade de participações por esporte

####  Análise de Gênero

* Distribuição de atletas por sexo

### Cada análise contém:

* Arquivo `.csv` com resultados
* Gráfico `.png`
* Arquivo `metadata.json`

---

##  Tecnologias Utilizadas

* Python
* Pandas
* PyArrow
* Matplotlib

---

##  Pipeline de Processamento

1. Ingestão dos dados na camada RAW
2. Criação de metadados
3. Transformação e limpeza dos dados
4. Conversão para Parquet (BRONZE)
5. Integração dos dados (JOINs)
6. Geração de análises (GOLD)

---

## Catálogo de Dados

O arquivo `metadata_schema.json` funciona como um **catálogo geral do Data Lake**, descrevendo:

* Estrutura das camadas
* Conjuntos de dados utilizados
* Organização do projeto

---

##  Objetivo Acadêmico

Este projeto foi desenvolvido como atividade prática com o objetivo de:

* Aplicar conceitos de Data Lake
* Trabalhar com múltiplas fontes de dados
* Realizar integração e análise de dados
* Organizar dados em camadas seguindo boas práticas

---

##  Resultado

O Data Lake final permite:

* Armazenamento estruturado de dados olímpicos
* Facilidade na geração de análises
* Base para futuras expansões e dashboards
---