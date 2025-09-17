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
- **cancelamentos_github.csv**: Versão de 1000 linhas para visualização no GitHub (68KB)
- **Resumo-Aula2.md**: Resumo dos conceitos e comandos da análise de dados

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
- **Jupyter Notebook**: Análise interativa
- **Git LFS**: Gerenciamento de arquivos grandes

## 🚀 Como Usar

1. Clone o repositório:
```bash
git clone https://github.com/ViniciusSavianDeArruda/Curso-Python.git
cd Curso-Python
```

2. Instale as dependências:
```bash
pip install pandas plotly pyautogui jupyter
```

3. Para baixar os arquivos grandes do Git LFS:
```bash
git lfs pull
```

4. Execute os scripts ou abra os notebooks conforme necessário.

---
*Curso de Python - Automação e Análise de Dados* 🐍📈