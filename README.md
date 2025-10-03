# Curso Python

Este repositório contém os projetos e exercícios do curso de Python.

## 📁 Estrutura do Projeto

### Aula 1 - Automação de Tarefas
- **aula.py**: Script de automação para cadastro de produtos usando PyAutoGUI
- **produtos.csv**: Base de dados dos produtos para cadastro
- **auxiliar.py**: Funções auxiliares para automação
- **ResumoAula1.md**: Resumo dos conceitos aprendidos

### Aula 2 - Análise de Dados
- **inicial.ipynb**: Notebook Jupyter com análise de cancelamentos de clientes
- **cancelamentos.csv**: Dataset completo com ~881k registros (58MB) - gerenciado via Git LFS
- **cancelamentos_sample.csv**: Amostra menor do dataset para testes
- **Resumo-Aula2.md**: Resumo dos conceitos e comandos da análise de dados

### Aula 3 - Inteligência Artificial e Previsões
- **inicial.ipynb**: Notebook com desenvolvimento de modelo de Machine Learning
- **clientes.csv**: Dataset com 100k clientes para análise de score de crédito
- **novos_clientes.csv**: Dados de novos clientes para fazer previsões
- **Resumo-Aula3.md**: Resumo completo dos conceitos de IA e Machine Learning

### Aula 4 - Desenvolvimento Web ✨
- **projeto1-chatbot-ia/**: ChatBot inteligente com Streamlit + OpenAI
  - `main.py`: ChatBot com IA real (GPT-4)
  - `demo.py`: Versão demonstrativa (sem API key)
  - `auxiliar.py`: Funções auxiliares
  - `requirements.txt`: Dependências automatizadas
- **projeto2-chat-web/**: Chat em tempo real com Flask + Socket.IO
  - `main.py`: Servidor web com WebSockets
  - `templates/index.html`: Interface do chat
  - `requirements.txt`: Dependências do Flask

## 📊 Sobre os Datasets

### Arquivos CSV Grandes
Os arquivos `cancelamentos.csv` e outros CSVs grandes são gerenciados pelo **Git LFS** (Large File Storage) para otimizar o repositório.

- **cancelamentos.csv**: Dataset completo (881.666 linhas, 58MB)
- **cancelamentos_github.csv**: Amostra de 1000 linhas para visualização fácil no GitHub

### Visualização dos Dados
- Para ver os dados no GitHub: use o arquivo `cancelamentos_github.csv`
- Para análises completas: clone o repositório e use `cancelamentos.csv`
- Para gráficos interativos: abra o notebook `inicial.ipynb`

## 🛠️ Tecnologias Utilizadas
- **Python 3.12**
- **Pandas**: Manipulação de dados
- **Plotly**: Visualizações interativas
- **PyAutoGUI**: Automação de interface
- **Scikit-learn**: Machine Learning e Inteligência Artificial
- **Jupyter Notebook**: Análise interativa e desenvolvimento de IA
- **Git LFS**: Gerenciamento de arquivos grandes
- **Streamlit**: Framework web para aplicações Python
- **Flask**: Micro-framework web com Socket.IO
- **OpenAI API**: Integração com GPT-4 para IA conversacional
- **WebSockets**: Comunicação em tempo real

## 🚀 Como Usar

1. Clone o repositório:
```bash
git clone https://github.com/ViniciusSavianDeArruda/Curso-Python.git
cd Curso-Python
```

2. Instale as dependências:
```bash
pip install pandas plotly pyautogui jupyter scikit-learn
```

3. Para baixar os arquivos grandes do Git LFS:
```bash
git lfs pull
```

4. Execute os scripts ou abra os notebooks conforme necessário.

## 🎯 Projetos Desenvolvidos

### 🤖 Aula 1: Automação de Processos
- Cadastro automático de produtos em sistemas web
- Automação de interface gráfica com PyAutoGUI

### 📊 Aula 2: Análise de Dados  
- Análise de cancelamentos de clientes
- Visualizações interativas com gráficos Plotly
- Identificação de padrões e insights nos dados

### 🧠 Aula 3: Inteligência Artificial
- Desenvolvimento de modelo de Machine Learning
- Previsão de Score de Crédito (Bom, OK, Ruim)
- Algoritmos: Random Forest e K-Nearest Neighbors
- Acurácia de modelos e aplicação em novos dados

### 🌐 Aula 4: Desenvolvimento Web
- **ChatBot IA**: Interface conversacional com GPT-4
- **Chat em Tempo Real**: WebSockets para comunicação instantânea
- **Streamlit**: Apps web interativas sem JavaScript
- **Flask + Socket.IO**: Servidor web com comunicação bidirecional

## 🚀 Como Executar os Projetos Web

### ChatBot Demonstração (sem API key)
```bash
cd "aula4-Desenvolvimento Web/projeto1-chatbot-ia"
streamlit run demo.py --server.port 8501
# Acesse: http://localhost:8501
```

### Chat Web em Tempo Real
```bash
cd "aula4-Desenvolvimento Web/projeto2-chat-web"
python main.py
# Acesse: http://localhost:5000
```

## 📱 Projetos Ativos

| 🎯 Projeto | 🌐 URL | ⚡ Status | 💻 Comando |
|------------|---------|-----------|------------|
| **ChatBot Demo** | `localhost:8501` | 🟢 Pronto | `streamlit run demo.py` |
| **Chat Web** | `localhost:5000` | 🟢 Pronto | `python main.py` |
| **IA Real** | `localhost:8501` | 🟡 API Key | `streamlit run main.py` |

---
*Curso de Python - Automação, Análise de Dados, IA e Desenvolvimento Web* 🐍📈🤖🌐