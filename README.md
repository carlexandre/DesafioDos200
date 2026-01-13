# Desafio dos 200 — Aplicação de Economia Gamificada

![Licença](https://img.shields.io/badge/License-MIT-blue)

Aplicação web interativa desenvolvida para auxiliar no **Desafio dos 200** (ou desafio de 1 a 200).  
A proposta é incentivar o hábito de economizar de forma simples e motivadora: o usuário deve guardar valores de **R$ 1,00 a R$ 200,00**, marcando cada valor conforme ele é economizado.

Ao completar toda a tabela, o total economizado será de **R$ 20.100,00**.

A aplicação permite o acompanhamento do progresso em tempo real e suporta múltiplos usuários, sendo ideal para uso individual, em casal ou em família, por meio de **códigos de desafio compartilhados**.

---

## Funcionalidades

- **Sincronização em tempo real** utilizando Firebase Firestore
- **Sistema de códigos de desafio** para compartilhamento do progresso entre usuários
- **Autenticação segura** com Firebase Authentication (Email/Senha)
- **Dashboard interativo**, contendo:
  - Tabela clicável de 1 a 200
  - Cálculo automático do valor economizado e do valor restante
  - Barra de progresso visual
- **Arquitetura SPA (Single Page Application)**, sem recarregamento de página
- **Layout responsivo**, adaptado para desktop e dispositivos móveis

---

## Tecnologias Utilizadas

- **HTML5**
- **JavaScript (ES6+)** — Vanilla JS com módulos
- **Tailwind CSS** — estilização moderna e responsiva via CDN
- **Firebase Authentication** — gerenciamento de usuários
- **Cloud Firestore** — banco de dados NoSQL em tempo real

---

## Como Utilizar

### Acesso Online

A aplicação pode ser acessada diretamente pelo GitHub Pages:

[https://carlexandre.github.io/DesafioDos200/](https://carlexandre.github.io/DesafioDos200/)

---

## Execução Local

Siga as etapas abaixo para configurar e executar o projeto em seu ambiente de desenvolvimento.

### 1. Clonar o Repositório

Abra o terminal e execute os comandos abaixo para obter o código-fonte:

```bash
git clone https://github.com/carlexandre/DesafioDos200.git
cd DesafioDos200
```

### 2. Configuração do Firebase

Este projeto utiliza o **Firebase** como backend. É necessário criar uma instância própria para obter as chaves de acesso.

1. Acesse o **Firebase Console** e crie um novo projeto.
2. **Authentication**:
   - No menu lateral, selecione **Authentication**
   - Ative o provedor de login **Email/Senha**
3. **Firestore Database**:
   - Selecione **Firestore Database**
   - Crie um banco de dados  
   - Para desenvolvimento, recomenda-se iniciar em **modo de teste**
4. **Obter Credenciais**:
   - Acesse **Configurações do Projeto** (ícone de engrenagem) → **Geral**
   - Na seção **Seus aplicativos**, adicione um aplicativo **Web**
   - Copie o objeto `firebaseConfig` gerado
   - Substitua as credenciais existentes no arquivo de configuração JavaScript da aplicação

---

### 3. Inicialização do Servidor

A aplicação foi construída utilizando **Módulos ES6** (`type="module"`).  
Devido às políticas de segurança dos navegadores (**CORS**), não é possível abrir o arquivo `index.html` diretamente pelo sistema de arquivos (`file://`).

É necessário servir a aplicação através de um **servidor HTTP local**.

#### Opção A — VS Code + Live Server (Recomendado)

1. Instale a extensão **Live Server** no Visual Studio Code
2. Abra o arquivo `index.html`
3. Clique no botão **Go Live** na barra de status inferior do editor

---

#### Opção B — Servidor Local com Python

Caso possua o **Python** instalado, execute o comando abaixo na raiz do projeto:

```bash
python -m http.server 8000
```

Em seguida, acesse:

```bash
http://localhost:8000
```
<p align="center">
Desenvolvido por <a href="https://github.com/carlexandre">Carlexandre</a>
</p>
