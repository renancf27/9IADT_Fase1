# 9IADT_Fase1
Grupo para o desafio Tech Challenge - Fase 1 

# Tech Challenge - Classificação de Câncer de Mama
## Visão Geral
Este projeto implementa um pipeline de machine learning para classificar tumores de mama como benignos ou malignos utilizando o dataset Breast Cancer Wisconsin (Diagnostic), disponível na UCI Machine Learning Repository.

## Objetivo
Desenvolver e avaliar modelos supervisionados capazes de prever o diagnóstico com base em características numéricas extraídas de imagens de aspirado por agulha fina (FNA).

## Dataset
Fonte: https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic)

##Notebook Tech Challenge
https://colab.research.google.com/drive/1QOF-LYYT3486OEfxN6jDCJ3Ptvq9r2ZJ?usp=sharing#scrollTo=US-TzilXlDXK

##Notebook Tech Challenge Desafio Extra
https://colab.research.google.com/drive/1ck7NXZDEjTLQmMx1s7A9-AVFTE8lyFyn?usp=sharing#scrollTo=ec0LgqsycZwl

Características:
- 569 amostras
- 30 atributos numéricos
- Variável alvo: `diagnosis` (B = benigno, M = maligno)

Observação:
A coluna `Unnamed: 32` deve ser removida, pois contém apenas valores nulos.

## Estrutura do Projeto

```
.
├── DocumentoEntregaTech ChallengeFase1.pdf
├── README.md
├── data.csv
├── relatorioTCDesafioExtra.pdf
├── relatorioTechChallenge.pdf
├── techchallenge.ipynb
├── techchallenge.py
├── techchallengeextra.ipynb
├── techchallengeextra.py
```

## Requisitos

- Python 3.8+ Manual de instalação Python: https://docs.python.org/3/tutorial/index.html

Instalação das dependências:

```bash
pip install numpy pandas seaborn matplotlib scikit-learn
!pip install shap -q
```

## Execução
Certifique-se de que o arquivo do dataset esteja nomeado como `data.csv` e localizado na raiz do projeto.

Executar:

```bash
python techchallenge.py
```

## Metodologia

### Preparação dos Dados
- Remoção de colunas irrelevantes (`id`, `Unnamed: 32`)
- Codificação da variável alvo com `LabelEncoder`
- Normalização com `StandardScaler`
- Divisão treino/teste com `stratify`

### Análise Exploratória
- Estatísticas descritivas
- Histogramas
- Boxplots para detecção de outliers
- Heatmap de correlação

### Modelos

#### Random Forest
- Pipeline com pré-processamento
- 100 árvores
- Execução paralela

#### K-Nearest Neighbors (KNN)
- k = 3
- Dados normalizados

### Avaliação
- Acurácia
- F1-score
- Precision
- Recall
- Matriz de confusão
- Classification report

## Resultados

Os modelos são avaliados em um conjunto de teste (20% dos dados). O Random Forest tende a apresentar melhor desempenho devido à sua capacidade de modelar relações não lineares.

## Autores

- Cristiano Roberto Câmara
- Eric Soares Dias
- Renan Costa Filgueiras
- Willian Gonçalves de Freitas
