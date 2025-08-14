# Projeto de Análise e Modelagem Preditiva de Consumo

## Descrição

Este projeto realiza análise exploratória de dados e modelagem preditiva para previsão de consumo baseado em dados climáticos e características dos clientes.

## Estrutura do Projeto

```
├── data/                           # Dados do projeto
│   ├── clientes.csv               # Dados originais dos clientes
│   ├── clima.csv                  # Dados originais do clima
│   ├── consumo.csv                # Dados originais de consumo
│   ├── clientes_tratado.csv       # Dados tratados dos clientes
│   ├── clima_tratado.csv          # Dados tratados do clima
│   ├── consumo_tratado.csv        # Dados tratados de consumo
│   └── dataset_modelagem.csv      # Dataset final para modelagem
├── notebooks/                      # Notebooks de análise
│   ├── 01_analise_exploratoria.ipynb
│   ├── 02_tratamento_dados.ipynb
│   ├── 03_duckdb.ipynb
│   ├── 04_modelagem_preditiva.ipynb
│   └── 05_pipeline_completo.ipynb
├── models/                         # Modelos treinados
│   └── pipeline_20250813_204748.pkl
├── dashboards/                     # Dashboards interativos
│   └── dashboard.ipynb
└── requirements.txt               # Dependências do projeto
```

## Ambiente e Configuração

### 1. Criação do Ambiente Virtual

```bash
python -m venv venv
```

### 2. Ativação do Ambiente

**Windows:**
```bash
venv\Scripts\activate
```

**Linux/macOS:**
```bash
source venv/bin/activate
```

### 3. Instalação das Dependências

```bash
pip install -r requirements.txt
```

## Bibliotecas Utilizadas

- **pandas** (>=2.0.0): Manipulação e análise de dados
- **numpy** (>=1.24.0): Computação numérica
- **matplotlib** (>=3.7.0): Visualização de dados
- **seaborn** (>=0.12.0): Visualização estatística
- **plotly** (>=5.15.0): Gráficos interativos
- **duckdb** (>=0.8.0): Banco de dados analítico
- **scikit-learn** (>=1.3.0): Machine learning
- **xgboost** (>=1.7.0): Gradient boosting
- **ipywidgets** (>=8.0.0): Widgets interativos para Jupyter

## Ordem de Execução

### 1. Análise Exploratória
```bash
jupyter notebook notebooks/01_analise_exploratoria.ipynb
```
Executa a análise inicial dos dados, visualizações e estatísticas descritivas.

### 2. Tratamento de Dados
```bash
jupyter notebook notebooks/02_tratamento_dados.ipynb
```
Realiza limpeza, transformação e preparação dos dados.

### 3. Análise com DuckDB
```bash
jupyter notebook notebooks/03_duckdb.ipynb
```
Executa consultas e análises usando DuckDB.

### 4. Modelagem Preditiva
```bash
jupyter notebook notebooks/04_modelagem_preditiva.ipynb
```
Desenvolve e treina modelos de machine learning.

### 5. Pipeline Completo
```bash
jupyter notebook notebooks/05_pipeline_completo.ipynb
```
Executa o pipeline completo de dados e modelagem.

### 6. Dashboard Interativo
```bash
jupyter notebook dashboards/dashboard.ipynb
```
Visualiza resultados através de um dashboard interativo.

## Uso

1. Clone ou baixe o projeto
2. Configure o ambiente conforme as instruções acima
3. Execute os notebooks na ordem especificada
4. Os modelos treinados serão salvos na pasta `models/`
5. Utilize o dashboard para visualizar os resultados

## Dados

O projeto utiliza três conjuntos de dados principais:
- **Clientes**: Informações dos clientes e suas características
- **Clima**: Dados meteorológicos (temperatura, umidade, sensação térmica)
- **Consumo**: Dados de consumo dos clientes

O dataset final (`dataset_modelagem.csv`) contém todas as variáveis integradas e preparadas para modelagem.

## Resultados

O modelo final é capaz de prever o consumo com base em:
- Dados climáticos (temperatura, umidade, sensação térmica)
- Características temporais (mês, dia da semana, dia do ano)
- Região do cliente
- Histórico de consumo (lags e médias móveis)
