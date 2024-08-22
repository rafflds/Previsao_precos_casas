# Previsão de Preços de Casas com PySpark
Este projeto demonstra o uso do PySpark para processar um conjunto de dados imobiliários e construir um modelo de aprendizado de máquina para prever os preços das casas. O processo inclui carregamento de dados, pré-processamento, treinamento de um modelo de regressão linear e avaliação do seu desempenho.

## Índice
* Requisitos
* Instalação
* Estrutura do Projeto
* Uso
* Visão Geral do Pipeline
* Avaliação do Modelo
* Conclusão
* Requisitos


## Para executar este projeto, você precisa ter o seguinte software instalado:
* Python 3.x
* Apache Spark (PySpark)
* Opcionalmente: Jupyter Notebook para desenvolvimento interativo
* Instalação
* Instalar PySpark:
* Se o PySpark não estiver instalado, você pode instalá-lo usando pip:

## Instalação
- pip install pyspark

**Clonar o Repositório:**
- [git clone https://github.com/seuusuario/previsao-precos-casas-pyspark.git
cd previsao-precos-casas-pyspark](https://github.com/rafflds/Previsao_precos_casas.git)

## Conjunto de Dados:
Certifique-se de que o arquivo house_prices.csv está disponível no diretório do projeto. Se não estiver, coloque o conjunto de dados na pasta raiz.

## Estrutura do Projeto
previsao-precos-casas-pyspark/
│
├── house_prices.csv         # O conjunto de dados usado para treinamento e teste
├── house_prices_pyspark.py  # O script Python principal para executar o projeto
├── README.md                # Este arquivo README
└── requirements.txt         # Lista de dependências (se aplicável)

## Uso
Para executar o projeto, você pode executar o script house_prices_pyspark.py diretamente. O script irá carregar os dados, pré-processá-los, treinar um modelo de aprendizado de máquina e avaliar seu desempenho.

## Executando o Script
- spark-submit house_prices_pyspark.py

## Saída Exemplo
O script exibirá o seguinte:
* O esquema do conjunto de dados.
* Análise estatística básica (média, mínimo, máximo, etc.) do conjunto de dados.
* Erro Médio Quadrático (RMSE) e R² do modelo no conjunto de teste.
* Uma amostra de preços reais vs. preços previstos.

## Visão Geral do Pipeline
### Carregamento de Dados:
O conjunto de dados é carregado de um arquivo CSV usando a API DataFrame do PySpark.

### Análise Exploratória de Dados (EDA):
O script exibe o esquema do conjunto de dados, estatísticas básicas e verifica valores ausentes.

### Pré-processamento de Dados:
* Remoção de colunas desnecessárias.
* Codificação de recursos categóricos usando StringIndexer.
* Montagem de todas as features em um único vetor usando VectorAssembler.
* Normalização de features numéricas usando StandardScaler.
* Treinamento do Modelo:
* Um modelo de Regressão Linear é treinado usando as features pré-processadas.

## Avaliação do Modelo:
O desempenho do modelo é avaliado usando as seguintes métricas:
* Erro Médio Quadrático (RMSE): Mede o erro de previsão do modelo.
* R²: Indica o quão bem o modelo se ajusta aos dados.
Essas métricas fornecem uma visão sobre a precisão do modelo na previsão dos preços das casas.

## Conclusão
Este projeto demonstra como usar o PySpark para pré-processamento de dados, engenharia de features e treinamento de modelos de aprendizado de máquina. O modelo de Regressão Linear treinado fornece uma base para prever os preços das casas com base em várias features.
