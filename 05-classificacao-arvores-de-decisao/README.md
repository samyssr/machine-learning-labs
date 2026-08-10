# Classificação de Medicamentos com Árvores de Decisão

Este projeto aplica o algoritmo de **Árvores de Decisão** para recomendar o medicamento ideal para pacientes com base em suas características clínicas e demográficas.


## 📌 Objetivos
* Prever a classe de medicamento (`Drug A`, `Drug B`, `Drug C`, `Drug X` ou `Drug Y`) adequada para cada perfil de paciente.
* Analisar a estrutura da árvore de decisão e entender a seleção de variáveis via **Ganho de Informação** e redução de **Entropia**.
* Apresentar visualizações claras e explicáveis do modelo (*Explainable AI*).


## 🛠️ Tecnologias Utilizadas
* **Python 3**
* **Pandas**: Manipulação e tratamento de dados.
* **Scikit-Learn**: Treinamento do modelo `DecisionTreeClassifier`, avaliação e exportação de regras.
* **Matplotlib**: Renderização visual da árvore de decisão.


## 📊 Principais Insights e Regras de Decisão

A análise da árvore gerada revelou regras diretas sobre os dados:

1. **Seleção da Variável Raiz (`Na_to_K`):**
   * A razão Sódio/Potássio (`Na_to_K`) foi escolhida como nó raiz porque seu corte inicial gerou a maior queda de entropia do dataset.
2. **Critério para Drug Y:**
   * Pacientes com razão $\text{Na\_to\_K} > 14.627$ são diretamente classificados como **`Drug Y`** (grupo isolado com entropia $0.0$).
3. **Outras Classes ($\text{Na\_to\_K} \le 14.627$):**
   * Os demais casos são subdivididos sequencialmente avaliando níveis de Pressão Arterial (`BP`), Idade (`Age`) e Colesterol.

*Desenvolvido por Samyr Sundfeld Razuck*
