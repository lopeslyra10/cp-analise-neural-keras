# Análise Comparativa de Modelos de Machine Learning (Keras vs Scikit-learn)

Este notebook apresenta a implementação e comparação de modelos de **Machine Learning** utilizando as bibliotecas **Keras** (para redes neurais) e **Scikit-learn** para duas tarefas distintas: **Classificação Multiclasse** e **Regressão**.

---

## 🔹 Exercício 1: Classificação Multiclasse ([**Wine Dataset**](https://archive.ics.uci.edu/dataset/109/wine))

Neste exercício, treinamos modelos para classificar vinhos em três classes diferentes com base em suas características químicas.

### Objetivo
Comparar o desempenho de uma **Rede Neural Keras** com um modelo **Scikit-learn (Regressão Logística)** na tarefa de classificação.

### Passos Realizados
1. **Carregamento e Preparação dos Dados**
    - O *Wine Dataset* foi carregado e dividido em conjuntos de treino e teste.
2. **Modelo Keras para Classificação**
    - Rede Neural Sequencial com camadas densas.
    - Funções de ativação: **ReLU** (ocultas) e **Softmax** (saída).
    - Otimizador: **Adam** | Função de perda: **categorical\_crossentropy**.
    - Treinamento nos dados de treino.
3. **Modelo Scikit-learn para Classificação**
    - Regressão Logística instanciada e treinada nos dados de treino.
4. **Avaliação e Comparação**
    - Ambos os modelos avaliados no conjunto de teste com a métrica **acurácia**.
    - Resultados comparados para determinar o melhor desempenho.

### Resultados (Resumo)
- **Keras (Rede Neural):** acurácia $\approx$ `{{acuracia_keras:.4f}}`
- **Scikit-learn (Regressão Logística):** acurácia $\approx$ `{{acuracia_lr:.4f}}`

**Conclusão:** O modelo **Scikit-learn** teve uma acurácia maior no conjunto de teste para esta tarefa de classificação.

---

## 🔹 Exercício 2: Regressão ([**California Housing Dataset**](https://scikit-learn.org/stable/datasets/real_world.html#california-housing-dataset))

Neste exercício, treinamos modelos para prever o valor médio das casas no estado da Califórnia com base em diversas características.

### Objetivo
Comparar o desempenho de uma **Rede Neural Keras** com um modelo **Scikit-learn (Regressão Linear)** na tarefa de regressão.

### Passos Realizados
1. **Carregamento e Preparação dos Dados**
    - O *California Housing Dataset* foi carregado e dividido em conjuntos de treino e teste.
2. **Modelo Keras para Regressão**
    - Rede Neural Sequencial com camadas densas.
    - Funções de ativação: **ReLU** (ocultas) e **Linear** (saída).
    - Otimizador: **Adam** | Função de perda: **MSE** (*Erro Quadrático Médio*).
    - Treinamento nos dados de treino.
3. **Modelo Scikit-learn para Regressão**
    - Regressão Linear instanciada e treinada nos dados de treino.
4. **Avaliação e Comparação**
    - Ambos os modelos avaliados com a métrica **RMSE** (*Root Mean Squared Error*).
    - Resultados comparados para verificar qual teve menor erro.

### Resultados (Resumo)
- **Keras (Rede Neural):** RMSE $\approx$ `{{rmse_keras:.4f}}`
- **Scikit-learn (Regressão Linear):** RMSE $\approx$ `{{rmse_lr:.4f}}`

**Conclusão:** O modelo **Keras** obteve menor RMSE no conjunto de teste, indicando desempenho ligeiramente melhor.

---

## Conclusão Geral
- Para **classificação**, a **Regressão Logística (Scikit-learn)** superou a Rede Neural em termos de acurácia.
- Para **regressão**, a **Rede Neural (Keras)** apresentou menor erro, sendo mais eficaz para prever valores contínuos.

---
