# 💳 Detecção de Fraude em Cartões: 51% Recall com K-Means
[![Kaggle](https://img.shields.io/badge/Kaggle-Dataset-blue.svg)](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
[![Python](https://img.shields.io/badge/Python-3.8+-yellow.svg)](https://www.python.org/)
[![Status](https://img.shields.io/badge/Status-Project%20Completed-green.svg)]()

## 📝 Visão Geral
Este projeto implementa um pipeline de **Machine Learning Não Supervisionado** para identificar transações fraudulentas em cartões de crédito. O desafio central é o desequilíbrio extremo dos dados (apenas 0.17% são fraudes). 

A solução utiliza **K-Means Clustering** para modelar o comportamento normal e identificar fraudes como *outliers* (anomalias), complementado por uma regra de negócio baseada no valor da transação (*Amount*).



## 🎯 Resultados de Impacto
| Métrica | Baseline (Top 0.2%) | Modelo Final (Híbrido) | Melhoria |
| :--- | :--- | :--- | :--- |
| **Recall (Fraudes Detetadas)** | 24.4% | **45.9%** | **+88%** |
| **Fraudes Salvas** | 120 | **226** | **+106 fraudes** |
| **Impacto Financeiro Est.** | $60,000 | **$113,000** | **+$53,000** |

## 🚀 Pipeline Técnico
O projeto foi estruturado em 4 fases críticas para garantir a precisão do risco:

1.  **Exploração de Dados (EDA):** Identificação de padrões onde 99% das transações legítimas são inferiores a $200, enquanto as fraudes apresentam comportamentos de valor atípicos.
2.  **Pré-processamento:** Normalização com `StandardScaler` e aplicação de **PCA (Principal Component Analysis)** para redução de dimensionalidade (essencial para visualização e performance do algoritmo).
3.  **Algoritmo K-Means:** Agrupamento de transações em 7 clusters distintos para definir a "norma" do comportamento do utilizador.
4.  **Deteção Híbrida de Anomalias:** Otimização do threshold de distância euclidiana combinado com uma regra de risco para transações acima de $500.
