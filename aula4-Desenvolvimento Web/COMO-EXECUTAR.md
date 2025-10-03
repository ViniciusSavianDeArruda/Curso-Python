# 🚀 Como Executar os Projetos da Aula 4

## ⚠️ **IMPORTANTE: Executar Projetos Separadamente**
Os dois projetos são servidores web diferentes e **NÃO podem** ser executados simultaneamente no mesmo terminal.

---

## 🤖 **Projeto 1: ChatBot IA**

### 📍 **Localização:**
```
aula4-Desenvolvimento Web/projeto1-chatbot-ia/
```

### 🏃‍♂️ **Como Executar:**
1. Abra um terminal **dedicado** para este projeto
2. Navegue até a pasta:
```bash
cd "aula4-Desenvolvimento Web\projeto1-chatbot-ia"
```
3. Execute o Streamlit:
```bash
streamlit run main.py
```
4. **Resultado:** Abrirá automaticamente em `http://localhost:8501`

### ⚙️ **Configuração Necessária:**
- Configure sua chave da API OpenAI no arquivo `main.py`
- Substitua `"sk-proj-..."` pela sua chave real

---

## 💬 **Projeto 2: Chat Web**

### 📍 **Localização:**
```
aula4-Desenvolvimento Web/projeto2-chat-web/
```

### 🏃‍♂️ **Como Executar:**
1. Abra um **novo terminal** (diferente do Projeto 1)
2. Navegue até a pasta:
```bash
cd "aula4-Desenvolvimento Web\projeto2-chat-web"
```
3. Execute o Flask:
```bash
python main.py
```
4. **Resultado:** Acesse manualmente `http://localhost:5000`

### 🌐 **Testando o Chat:**
- Abra várias abas do navegador em `http://localhost:5000`
- Digite mensagens em uma aba
- Veja as mensagens aparecerem em todas as abas simultaneamente!

---

## 🚫 **Erros Comuns e Soluções**

### **Erro: "signal only works in main thread"**
**Causa:** Tentando executar Flask dentro do Streamlit
**Solução:** Execute cada projeto em terminal separado

### **Erro: "Port already in use"**
**Causa:** Tentando executar dois servidores na mesma porta
**Solução:** 
- Feche um dos projetos antes de executar o outro
- Ou use portas diferentes (5000 para Flask, 8501 para Streamlit)

### **Erro: "OpenAI API Key not found"**
**Causa:** Chave da API não configurada
**Solução:** 
1. Registre-se em https://platform.openai.com/
2. Obtenha sua API key
3. Substitua no código do `main.py`

---

## 📋 **Checklist de Execução**

### **Antes de executar qualquer projeto:**
- [ ] Dependências instaladas (`pip install -r requirements.txt`)
- [ ] Terminal limpo (sem outros servidores rodando)
- [ ] Pasta correta selecionada

### **Para o ChatBot IA:**
- [ ] API Key da OpenAI configurada
- [ ] Comando: `streamlit run main.py`
- [ ] Acesso: `http://localhost:8501`

### **Para o Chat Web:**
- [ ] Terminal separado aberto
- [ ] Comando: `python main.py`
- [ ] Acesso: `http://localhost:5000`

---

## 🎯 **Dicas de Uso**

1. **Execute apenas um projeto por vez** se você é iniciante
2. **Use terminais separados** para projetos simultâneos
3. **Pare servidores** com `Ctrl+C` antes de trocar de projeto
4. **Recarregue a página** se algo não funcionar

---

*💡 Dica: Para desenvolvedores avançados, é possível executar ambos simultaneamente usando portas diferentes!*