# 🚗 Predição de Emissão de CO2 com Regressão Linear Múltipla
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/samyssr/regressao-linear-multipla-emissao-co2/blob/main/Multiple_Linear_Regression.ipynb)

Projeto desenvolvido para estimar e analisar os níveis de emissão de CO2 em veículos utilizando técnicas de Machine Learning em Python.



## 📌 Sobre o Projeto
Este repositório contém a implementação de um modelo de **Regressão Linear Múltipla** utilizando a biblioteca **Scikit-Learn**. O objetivo é prever as emissões de dióxido de carbono ($CO_2$) a partir de características dos veículos, como o tamanho do motor (*Engine Size*) e o consumo combinado de combustível (*Fuel Consumption MPG*).



## 🛠️ Tecnologias e Bibliotecas Utilizadas
* **Python 3**
* **Pandas**: Manipulação e tratamento de dados
* **NumPy**: Operações com vetores e matrizes
* **Matplotlib**: Visualização de dados e gráficos 3D
* **Scikit-Learn**: Treinamento do modelo, predições e métricas de avaliação



## 📊 Estrutura e Funcionalidades
1. **Análise Exploratória e Pré-processamento:**
   * Seleção e tratamento das *features* preditivas no DataFrame.
   * Visualizações com Matriz de Dispersão (*Scatter Matrix*).
2. **Modelagem:**
   * Separação de conjuntos de treino e teste com `train_test_split`.
   * Ajuste do plano de regressão aos dados com `LinearRegression`.
3. **Visualização Tridimensional (3D):**
   * Plotagem interativa em 3D exibindo os pontos observados (acima e abaixo do plano) juntamente com a superfície do modelo ajustado.
4. **Avaliação do Modelo:**
   * Validação por métricas estatísticas: MAE, MSE e $R^2$-score.
