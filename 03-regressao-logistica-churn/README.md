# 📊 Predição de Churn de Clientes com Regressão Logística

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/samyssr/regressao-logistica-predicao-churn/blob/main/Logistic_Regression.ipynb)

Projeto desenvolvido para prever a probabilidade de cancelamento de serviços (*churn*) por clientes de telecomunicações utilizando o algoritmo de **Regressão Logística**.


## 📌 Sobre o Projeto
O objetivo deste estudo é identificar padrões comportamentais e demográficos que indicam o risco de evasão de clientes. O pipeline contempla desde a seleção de atributos (*feature selection*) até o cálculo das probabilidades de classe e métricas de desempenho probabilístico.


## 🛠️ Tecnologias e Bibliotecas Utilizadas
* **Python 3**
* **Pandas**: Manipulação e limpeza de dados
* **NumPy**: Estruturação de matrizes numéricas
* **Scikit-Learn**:
  * `StandardScaler`: Normalização e padronização das features
  * `train_test_split`: Divisão dos dados em treino e teste
  * `LogisticRegression`: Construção do modelo de classificação
  * `log_loss`: Avaliação da calibração de probabilidades do modelo


## 📊 Etapas do Projeto
1. **Tratamento e Seleção de Features:**
   * Mapeamento de variáveis demográficas e de consumo (como `tenure`, `age`, `address`, `income`, `ed`, `employ`, `equip`).
   * Conversão de tipos de dados para inteiros e isolamento do target `churn`.
2. **Padronização dos Dados:**
   * Uso do `StandardScaler` para colocar todas as variáveis preditivas na mesma escala.
3. **Treinamento e Predição:**
   * Ajuste do modelo com solver `liblinear`.
   * Geração de predições diretas (`yhat`) e estimativas de probabilidade (`yhat_prob`).
4. **Experimentos de Engenharia de Features:**
   * Análise do impacto da alteração de atributos na métrica **Log Loss**.
