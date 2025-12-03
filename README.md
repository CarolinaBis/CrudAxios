# CRUD React com Axios - Sistema de Gerenciamento de Usuários

Um aplicativo web completo de CRUD (Create, Read, Update, Delete) construído com React.js, utilizando Axios para comunicação com API e React Router para navegação.

## Funcionalidades

- **Create** - Adicionar novos usuários
- **Read** - Visualizar lista de usuários e detalhes individuais
- **Update** - Editar informações de usuários existentes
- **Delete** - Remover usuários com confirmação
- **Responsivo** - Interface adaptável a diferentes dispositivos

## Tecnologias Utilizadas

- **React.js 18+** - Biblioteca JavaScript para interfaces
- **React Router DOM** - Navegação entre páginas
- **Axios** - Cliente HTTP para requisições à API
- **MockAPI.io** - API REST fake para dados de teste
- **Bootstrap 5** - Framework CSS para estilização
- **React Hooks** - useState, useEffect, useParams, useNavigate

## Estrutura do Projeto

```
src/
├── components/
│   ├── Home.jsx       # Lista todos os usuários (página inicial)
│   ├── Create.jsx     # Formulário para criar novo usuário
│   ├── Read.jsx       # Detalhes de um usuário específico
│   └── Update.jsx     # Formulário para editar usuário
├── App.js            # Configuração das rotas
└── ...               # Outros arquivos do projeto
```

## 🚀 Instalação e Configuração

1. **Clone o repositório ou copie os arquivos**

2. **Instale as dependências:**
```bash
npm install axios react-router-dom bootstrap
```

3. **Configure o Bootstrap no seu projeto:**
Adicione no arquivo principal (index.js ou App.js):
```javascript
import 'bootstrap/dist/css/bootstrap.min.css';
```

4. **Configure o React Router:**
No seu `App.js`:
```jsx
import { BrowserRouter, Routes, Route } from 'react-router-dom';
import Home from './components/Home';
import Create from './components/Create';
import Read from './components/Read';
import Update from './components/Update';

function App() {
  return (
    <BrowserRouter>
      <Routes>
        <Route path='/' element={<Home />} />
        <Route path='/create' element={<Create />} />
        <Route path='/read/:id' element={<Read />} />
        <Route path='/update/:id' element={<Update />} />
      </Routes>
    </BrowserRouter>
  );
}
```

## Endpoints da API

A aplicação utiliza uma API mock gratuita:

- **Base URL:** `https://69307f5d778bbf9e0071a5f4.mockapi.io/CrudAxios/users`
- **GET** `/` - Listar todos os usuários
- **GET** `/:id` - Buscar usuário específico
- **POST** `/` - Criar novo usuário
- **PUT** `/:id` - Atualizar usuário
- **DELETE** `/:id` - Remover usuário

## Como Usar

### 1. Visualizar Usuários
- Acesse a página inicial (`/`) para ver todos os usuários cadastrados
- Cada usuário exibe: ID, Nome, Email, Celular e opções de ação

### 2. Criar Novo Usuário
- Clique no botão **"NOVO"**
- Preencha o formulário com:
  - Nome
  - Email
  - Celular
- Clique em **"Enviar"**

### 3. Ver Detalhes
- Clique no botão **"Ler"** em qualquer usuário
- Visualize informações detalhadas do usuário selecionado

### 4. Editar Usuário
- Clique no botão **"Editar"** em qualquer usuário
- Modifique os campos desejados
- Clique em **"Atualizar"**

### 5. Excluir Usuário
- Clique no botão **"Apagar"** em qualquer usuário
- Confirme a exclusão no diálogo de confirmação

### Mudar API
Para usar uma API diferente, altere a URL base em todos os componentes:
```javascript
const API_URL = 'https://sua-api.com/usuarios';
```

## Scripts Disponíveis

No projeto criado com Create React App:

```bash
npm start    # Inicia o servidor de desenvolvimento
npm build    # Cria build de produção
npm test     # Executa testes
npm eject    # Ejetar configurações (irreversível)
```
