# 🤖 Resumo da Aula 3 - Inteligência Artificial e Previsões

## 📋 **Objetivo do Projeto**
Criar um sistema de **Score de Crédito** usando Machine Learning para classificar automaticamente clientes em:
- **Good** (Boa) - Baixo risco
- **Standard** (OK) - Médio risco  
- **Poor** (Ruim) - Alto risco

---

## 🛠️ **Tecnologias Utilizadas**
- **Python 3.12**
- **Pandas** - Manipulação de dados
- **Scikit-learn** - Machine Learning
- **Jupyter Notebook** - Desenvolvimento interativo

---

## 📊 **Base de Dados**
- **Arquivo:** `clientes.csv`
- **Registros:** 100.000 clientes
- **Colunas:** 25 variáveis (idade, profissão, salário, etc.)
- **Target:** `score_credito` (Good, Standard, Poor)

---

## 🔧 **Passo a Passo do Desenvolvimento**

### **1️⃣ Importação e Exploração dos Dados**
```python
import pandas as pd

# Carregar dados
tabela = pd.read_csv("clientes.csv")
display(tabela)

# Verificar tipos de dados
display(tabela.info())
```

### **2️⃣ Preparação dos Dados**
**Problema:** Algoritmos de ML não trabalham com texto, apenas números.

**Solução:** Usar `LabelEncoder` para converter variáveis categóricas:

```python
from sklearn.preprocessing import LabelEncoder

# Converter profissão (texto → números)
codificador_profissao = LabelEncoder()
tabela["profissao"] = codificador_profissao.fit_transform(tabela["profissao"])

# Converter mix_credito
codificador_credito = LabelEncoder()
tabela["mix_credito"] = codificador_credito.fit_transform(tabela["mix_credito"])

# Converter comportamento_pagamento
codificador_pagamento = LabelEncoder()
tabela["comportamento_pagamento"] = codificador_pagamento.fit_transform(tabela["comportamento_pagamento"])
```

### **3️⃣ Separação dos Dados**
```python
from sklearn.model_selection import train_test_split

# Definir variáveis
y = tabela["score_credito"]  # O que queremos prever
x = tabela.drop(columns=["score_credito", "id_cliente"])  # Dados para previsão

# Dividir em treino (70%) e teste (30%)
x_treino, x_teste, y_treino, y_teste = train_test_split(x, y, test_size=0.3)
```

### **4️⃣ Criação e Treinamento dos Modelos**
**Dois algoritmos de Machine Learning:**

```python
from sklearn.ensemble import RandomForestClassifier
from sklearn.neighbors import KNeighborsClassifier

# Criar os modelos
modelo_arvoredecisao = RandomForestClassifier()  # Random Forest
modelo_knn = KNeighborsClassifier()              # K-Nearest Neighbors

# Treinar os modelos
modelo_arvoredecisao.fit(x_treino, y_treino)
modelo_knn.fit(x_treino, y_treino)
```

### **5️⃣ Avaliação dos Modelos**
```python
from sklearn.metrics import accuracy_score

# Fazer previsões
previsao_arvoredecisao = modelo_arvoredecisao.predict(x_teste)
previsao_knn = modelo_knn.predict(x_teste)

# Calcular acurácia
acuracia_rf = accuracy_score(y_teste, previsao_arvoredecisao)
acuracia_knn = accuracy_score(y_teste, previsao_knn)

print(f"Random Forest: {acuracia_rf:.2%}")
print(f"KNN: {acuracia_knn:.2%}")
```

### **6️⃣ Aplicação em Novos Clientes**
```python
# Carregar novos clientes
tabela_novos_clientes = pd.read_csv("novos_clientes.csv")

# Aplicar as mesmas transformações
tabela_novos_clientes["profissao"] = codificador_profissao.transform(tabela_novos_clientes["profissao"])
tabela_novos_clientes["mix_credito"] = codificador_credito.transform(tabela_novos_clientes["mix_credito"])
tabela_novos_clientes["comportamento_pagamento"] = codificador_pagamento.transform(tabela_novos_clientes["comportamento_pagamento"])

# Fazer previsões com o melhor modelo
nova_previsao = modelo_arvoredecisao.predict(tabela_novos_clientes)
print(nova_previsao)
```

---

## 🧠 **Conceitos de Machine Learning Aprendidos**

### **Algoritmos Utilizados:**
1. **Random Forest** (Floresta Aleatória)
   - Ensemble de múltiplas árvores de decisão
   - Mais robusto e preciso
   - Geralmente melhor performance

2. **K-Nearest Neighbors (KNN)**
   - Baseado em vizinhos próximos
   - Simples e intuitivo
   - Sensível à escala dos dados

### **Métricas de Avaliação:**
- **Acurácia:** Percentual de previsões corretas
- **Train/Test Split:** Divisão para evitar overfitting

### **Pré-processamento:**
- **Label Encoding:** Converter texto em números
- **Feature Selection:** Remover colunas irrelevantes (ID)

---

## 📈 **Resultados Esperados**
- Modelo capaz de classificar score de crédito automaticamente
- Acurácia típica: 80-95% dependendo dos dados
- Sistema pronto para produção em bancos

---

## 🚀 **Comandos PowerShell para Executar**

### **Instalar Bibliotecas:**
```powershell
pip install pandas scikit-learn jupyter
```

### **Executar Notebook:**
```powershell
cd "c:\Users\Adminstrador\OneDrive\Desktop\Curso Python\aula3-Inteligencia Artificial e Previsoes"
jupyter notebook inicial.ipynb
```

---

## 🎯 **Aplicações Práticas**
- **Bancos:** Aprovação automática de empréstimos
- **Fintechs:** Análise de risco de crédito
- **E-commerce:** Limite de crédito dinâmico
- **Seguradoras:** Precificação de produtos

---

*📚 **Aula 3 - Inteligência Artificial e Previsões** - Curso Python Completo*