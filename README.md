# 🚢 Titanic Survival Prediction  
### Kaggle Competition – Machine Learning from Disaster

Este projeto tem como objetivo prever a sobrevivência dos passageiros do Titanic utilizando técnicas de Machine Learning. O desenvolvimento foi estruturado em etapas, permitindo avaliar como diferentes estratégias de tratamento e modelagem impactam o desempenho final.

---

## 🎯 Objetivo

Construir modelos preditivos capazes de estimar a probabilidade de sobrevivência com base em variáveis demográficas e socioeconômicas, analisando a evolução dos resultados ao longo das melhorias aplicadas.

---

## 🔬 Desenvolvimento do Projeto

O projeto foi dividido em **cinco etapas progressivas**, cada uma focada em melhorias específicas no pipeline.

---

## 🧱 Etapa 1 – Modelo Inicial

Nesta etapa foi aplicado apenas o tratamento básico dos dados, com o objetivo de estabelecer um **baseline** para comparação.

### ✔ O que foi feito:

- Análise exploratória utilizando **ydata-profiling**
- Remoção de colunas com alta cardinalidade
- Tratamento de valores ausentes:
  - Média para variáveis numéricas
  - Moda para variáveis categóricas
- Exclusão de colunas textuais
- Treinamento dos modelos:
  - **Árvore de Decisão**
  - **K-Nearest Neighbors (KNN)**
  - **Regressão Logística**
- Avaliação com:
  - **Acurácia**
  - **Matriz de confusão**

**Score público no Kaggle:** `0.66746`

---

## 🧩 Etapa 2 – Tratamento das Variáveis Categóricas

O foco foi incorporar corretamente as variáveis categóricas ao modelo.

### ✔ Melhorias implementadas:

- Transformações personalizadas com `lambda`
- Codificação utilizando **OneHotEncoder**
- Manutenção dos mesmos algoritmos para comparação controlada

**Score público no Kaggle:** `0.76555`

📈 Houve ganho significativo apenas com o tratamento adequado das variáveis categóricas.

---

## 🧠 Etapa 3 – Engenharia de Atributos

Nesta fase, o objetivo foi aprofundar a compreensão dos dados e extrair informações adicionais relevantes.

### ✔ Ajustes realizados:

- Padronização das variáveis `Age` e `Fare`
- Criação de novas features:
  - `FamilySize = SibSp + Parch + 1`
  - `IsAlone` (indicador binário)
- Análise de correlação para seleção de variáveis mais relevantes

Os mesmos modelos foram mantidos para garantir consistência na comparação.

**Score público no Kaggle:** `0.77033`

---

## 🤖 Etapa 4 – Modelos Mais Complexos

Foram mantidas todas as variáveis e testados modelos com maior capacidade de ajuste.

### ✔ Algoritmos avaliados:

- **Regressão Logística**
- **Random Forest**
- **MLPClassifier (Rede Neural)**

O **MLPClassifier** apresentou a maior acurácia na validação, porém teve pior desempenho na submissão final.

**Score público no Kaggle:** `0.69856`

⚠ Isso indica provável **overfitting**, com perda de capacidade de generalização.

---

## ⚙️ Etapa 5 – Otimização com GridSearchCV

Aplicação do **GridSearchCV** para encontrar os melhores hiperparâmetros dos modelos testados na etapa anterior.

Após a otimização:

- O modelo com melhor desempenho foi o **Random Forest**
- Houve melhora consistente tanto na validação quanto na submissão

**Score público no Kaggle:** `0.78229`

---

## 📊 Evolução dos Resultados

| Etapa | Estratégia | Score Público |
|-------|------------|--------------|
| 1 | Modelo básico | 0.66746 |
| 2 | Tratamento categórico | 0.76555 |
| 3 | Engenharia de atributos | 0.77033 |
| 4 | Modelos complexos | 0.69856 |
| 5 | GridSearchCV | **0.78229** |

---

## 🧠 Principais Aprendizados

- O tratamento adequado das variáveis categóricas teve grande impacto no desempenho.
- Engenharia de atributos pode ser mais relevante que aumentar a complexidade do modelo.
- Modelos mais complexos não garantem melhor generalização.
- Ajuste de hiperparâmetros é essencial para extrair o melhor desempenho dos modelos.
- Experimentação estruturada facilita a análise e a evolução do pipeline.

---

## 🛠 Tecnologias Utilizadas

- Python
- Pandas
- NumPy
- Scikit-Learn
- Matplotlib
- Seaborn
- ydata-profiling
