# 🚗 Previsão de Emissão de CO2 com Regressão Linear Simples
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/samyssr/regressao-linear-emissao-co2/blob/main/regressao_linear_co2.ipynb)

## 📌 Descrição do Projeto
Este projeto analisa e prevê a emissão de dióxido de carbono ($\text{CO}_2$) de veículos com base em características do motor (como tamanho do motor `ENGINESIZE` e número de cilindros `CYLINDERS`), utilizando técnicas de Regressão Linear Simples com a biblioteca `scikit-learn`.


## 🛠️ Tecnologias e Bibliotecas Utilizadas
* **Linguagem:** Python 3
* **Análise de Dados:** `pandas`, `numpy`
* **Visualização:** `matplotlib`
* **Machine Learning:** `scikit-learn` (`LinearRegression`, `train_test_split`, `metrics`)

## 📊 Estrutura e Métricas do Modelo

### 1. Preparação dos Dados
* Divisão dos dados em treino (80%) e teste (20%) utilizando `train_test_split`.
* Uso de estruturas bidimensionais (`DataFrame 2D`) para tratamento direto dos arrays.

### 2. Métricas de Avaliação (*Evaluation*)
O desempenho do modelo é medido pelas seguintes estatísticas:
* **MAE (Mean Absolute Error):** Erro médio absoluto em escala real.
* **MSE (Mean Squared Error):** Erro quadrático médio.
* **RMSE (Root Mean Squared Error):** Raiz do erro quadrático médio.
* **$R^2$ Score:** Proporção da variância explicada pelo modelo.

## 📁 Arquivos do Repositório
* `regressao_linear_co2.ipynb`: Notebook completo com o código, gráficos e exercícios práticos resolvidos.
* `README.md`: Documentação explicativa do repositório.
