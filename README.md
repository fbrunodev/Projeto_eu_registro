# Projeto: eu_registro

Projeto de classificação de marcas do INPI com foco em ciência de dados e machine learning.

## Objetivo
Desenvolver um modelo de classificação capaz de prever se uma marca será concedida ou não com base em dados históricos disponibilizados.

## 📚 Tecnologias Utilizadas
- Python
- Pandas, Numpy
- Scikit-learn
- imblearn
- Gensim (Word2Vec)
- Matplotlib, Seaborn
- Google Colab

## Dados Utilizados
- `dum_processos.csv`
- `dump_processos_despacho.csv`
- `conclusoes_parecer.csv`

## Etapas do Projeto

### 1. Análise Inicial
- Identificação de quebras de linha e problemas de leitura nos CSVs.
- Reescrita dos arquivos para possibilitar leitura no Google Colab.

### 2. Limpeza e Pré-processamento
- Dataset com 18 colunas e cerca de 5 milhões de linhas.
- Presença de dados nulos em até 80% de algumas colunas.
- Remoção de colunas irrelevantes e com dados faltantes.
- Tratamento de datas e separação em `ano`, `mês`, `dia`.
- Limpeza básica de texto (remoção de acentos, pontuação, espaços extras).

### 3. Transformação dos Dados
- Vetorização de texto com **TF-IDF** e remoção de *stopwords*.
- Tratamento de colunas categóricas com **One-hot encoding**.
- Normalização de dados numéricos com **StandardScaler**.

### 4. Treinamento de Modelos
- Redução do dataset para 100 mil amostras devido a limitações do Google Colab.
- Testes com os seguintes modelos:
  - **Naive Bayes** (baixo desempenho)
  - **Logistic Regression**
  - **XGBoost**
  - **RandomForest** (melhor desempenho)

### 5. Balanceamento de Classes
- Variável-alvo `marca_add` desbalanceada.
- Aplicação de **RandomUnderSampler** (imblearn) para equilibrar as classes.

### 6. Otimizações
- Substituição de **TF-IDF** por **Word2Vec** para melhor representação semântica dos textos.

## Resultado Final
O
