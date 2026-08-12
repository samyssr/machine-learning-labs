# Previsão de Gorjetas de Táxi com Árvores de Regressão

Este projeto explora a aplicação do algoritmo de **Árvores de Regressão** (`DecisionTreeRegressor`) para estimar o valor contínuo das gorjetas em corridas de táxi. O estudo foca no impacto da profundidade da árvore (`max_depth`), no fenômeno de *overfitting* vs. *underfitting* e na eliminação de ruídos via seleção de atributos (*Feature Selection*).



## 📌 Objetivos
* Prever uma variável numérica contínua (`tip_amount`) com base no histórico de corridas.
* Avaliar o desempenho do modelo utilizando as métricas **MSE** (*Mean Squared Error*) e **$R^2$ Score** (*Coeficiente de Determinação*).
* Analisar o impacto da variação de profundidade (`max_depth`) na capacidade de generalização do algoritmo.
* Filtrar e remover atributos irrelevantes com base na matriz de correlação.



## 🛠️ Tecnologias Utilizadas
* **Python 3**
* **Pandas & NumPy**: Manipulação, limpeza e transformação matricial dos dados.
* **Scikit-Learn**: Algoritmo `DecisionTreeRegressor`, avaliação de métricas e divisão de treino/teste.


## 📊 Comparativo de Experimentos

Abaixo está o resumo numérico das iterações realizadas durante o ajuste fino do modelo:

| Experimento | Hiperparâmetros | Atributos (*Features*) | MSE (Erro) | $R^2$ Score | Diagnóstico |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Modelo Base** | `max_depth = 8` | Todas as colunas | `24.555` | `0.028` ($2,8\%$) | Underfitting / Ruído presente |
| **Teste 1** | `max_depth = 12` | Todas as colunas | `26.459` | `-0.047` | **Overfitting Severo** |
| **Teste 2** | `max_depth = 4` | Todas as colunas | `24.412` | `0.034` ($3,4\%$) | Ponto de menor variância |
| **Teste 3 (Final)**| `max_depth = 4` | **Sem ruídos** (4 colunas removidas) | `24.468` | `0.031` ($3,1\%$) | **Modelo enxuto e otimizado** |


## 💡 Principais Aprendizados e Conclusões

1. **Risco de Overfitting em Árvores Profundas:**
   * Aumentar o `max_depth` para 12 fez o $R^2$ cair para **$-0.047$** (negativo). O modelo decorou os dados de treino e perdeu completamente a capacidade de prever dados novos.
2. **Eficiência da Seleção de Atributos (*Feature Selection*):**
   * A remoção das variáveis sem correlação (`payment_type`, `VendorID`, `store_and_fwd_flag` e `improvement_surcharge`) manteve o $R^2$ estável na casa dos $3,1\%$. Isso provou que essas variáveis atuavam apenas como ruído no modelo.
3. **Necessidade de Métodos *Ensemble*:**
   * Uma única Árvore de Regressão atingiu um teto estrutural de explicabilidade ($\approx 3,1\%$). Em cenários reais de regressão com dados complexos e ruidosos, é necessário utilizar algoritmos baseados em múltiplos estimadores, como **Random Forest** ou **XGBoost**, para alcançar métricas elevadas.
