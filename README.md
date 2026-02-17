# 🚢 Titanic Survival Prediction  
## Kaggle Competition Project

**Competição:** Titanic - **[Machine Learning from Disaster](https://www.kaggle.com/competitions/titanic)**

---

## 📌 Objetivo

Desenvolver modelos de **Machine Learning** capazes de prever a sobrevivência de passageiros do Titanic com base em variáveis demográficas e socioeconômicas.

O projeto foi estruturado em múltiplas etapas evolutivas para avaliar o impacto de:

- Pré-processamento
- Engenharia de atributos
- Seleção de modelos
- Complexidade algorítmica
- Risco de overfitting

---

# 🔎 Metodologia

O desenvolvimento foi dividido em quatro etapas principais.

---

## 🔹 Etapa 1 — Modelo Baseline

O objetivo inicial foi estabelecer um modelo de referência com o mínimo de tratamento.

### ✔ Procedimentos

- Análise exploratória com *ydata-profiling*
- Remoção de colunas com alta cardinalidade
- Tratamento de valores ausentes:
  - Média para variáveis numéricas
  - Moda para variáveis categóricas
- Remoção de variáveis textuais
- Treinamento com:
  - Decision Tree
  - KNN
  - Logistic Regression
- Avaliação com:
  - *Accuracy*
  - *Confusion Matrix*

**Public Score:** `0.66746`

---

## 🔹 Etapa 2 — Tratamento de Variáveis Categóricas

Foco na incorporação correta das variáveis textuais ao modelo.

### ✔ Melhorias

- Transformações com `lambda`
- Codificação com *OneHotEncoder*
- Manutenção dos mesmos algoritmos para comparação consistente

**Public Score:** `0.76555`

📈 *Ganho significativo ao tratar adequadamente variáveis categóricas.*

---

## 🔹 Etapa 3 — Engenharia de Features e Otimização

Nesta etapa, aprofundamos a análise de domínio para criar variáveis mais informativas.

### ✔ Ajustes aplicados

**1️⃣ Escalonamento**
- Padronização das variáveis `Age` e `Fare`

**2️⃣ Engenharia de atributos**

A partir de:
- `SibSp` (irmãos/cônjuges a bordo)
- `Parch` (pais/filhos a bordo)

Foram criadas:
- `FamilySize` (total de familiares)
- `IsAlone` (indicador binário)

**3️⃣ Análise de correlação**
- Seleção de variáveis com maior relevância estatística

Modelos utilizados:
- Decision Tree
- KNN
- Logistic Regression

**Public Score:** `0.77033`

📈 *Melhoria incremental*

