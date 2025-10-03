# 💬 Projeto 2: Chat Web em Tempo Real

## 📋 Descrição
Sistema de chat web em tempo real desenvolvido com Flask e WebSockets, permitindo múltiplos usuários conversarem simultaneamente.

## 🛠️ Tecnologias
- **Flask**: Framework web Python
- **Flask-SocketIO**: WebSockets para comunicação em tempo real
- **HTML/CSS/JavaScript**: Frontend do chat
- **WebSockets**: Protocolo de comunicação bidirecional

## 📦 Instalação

1. Instale as dependências:
```bash
pip install -r requirements.txt
```

## 🚀 Como Executar

⚠️ **IMPORTANTE:** Execute em um terminal separado, não junto com outros servidores web.

```bash
# Navegue até esta pasta
cd "aula4-Desenvolvimento Web\projeto2-chat-web"

# Execute o Flask
python main.py
```

Acesse o chat manualmente em `http://localhost:5000`

## ⚙️ Funcionalidades
- ✅ Chat em tempo real
- ✅ Múltiplos usuários simultâneos
- ✅ Interface responsiva
- ✅ Mensagens broadcast para todos
- ✅ Conexão via WebSockets

## 📂 Estrutura de Arquivos
```
projeto2-chat-web/
├── main.py                 # Servidor Flask
├── requirements.txt        # Dependências
├── README.md              # Documentação
└── templates/
    ├── index.html         # Interface do chat
    └── homepage.html      # Página inicial
```

## 📝 Como Usar
1. Execute o servidor Python
2. Abra o navegador e acesse `http://localhost:5000`
3. Digite seu nome/nickname
4. Comece a conversar!
5. Abra várias abas para simular múltiplos usuários

## 🌐 Conceitos Aprendidos
- **Flask Routes**: Criação de rotas web
- **WebSockets**: Comunicação em tempo real
- **Frontend/Backend**: Integração entre client e server
- **Broadcasting**: Envio de mensagens para múltiplos clientes

---
*Projeto desenvolvido durante o Curso de Python - Aula 4*