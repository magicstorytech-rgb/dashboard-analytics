# Dashboard Analytics TRIPE v10.7

Dashboard em tempo real para monitoramento de funil de vendas com Firebase.

## Estrutura do Projeto

```
dashboard-html/
├── index.html          # Página principal (único arquivo HTML)
├── vercel.json         # Configuração do Vercel
├── .gitignore          # Arquivos a ignorar no Git
└── README.md           # Este arquivo
```

## Como Fazer Deploy no Vercel

### Passo 1: Criar Repositório no GitHub

1. Acesse [github.com](https://github.com) e faça login
2. Clique no ícone `+` no canto superior direito
3. Selecione "New repository"
4. Nomeie como `dashboard-analytics` (ou outro nome de sua preferência)
5. Deixe como "Public" (para Vercel conseguir acessar)
6. Clique em "Create repository"

### Passo 2: Fazer Upload dos Arquivos

Você tem duas opções:

#### Opção A: Usando Git (Recomendado)

```bash
# No terminal, navegue até a pasta do projeto
cd /caminho/para/dashboard-html

# Inicializar repositório Git
git init

# Adicionar todos os arquivos
git add .

# Fazer commit inicial
git commit -m "Initial commit - Dashboard Analytics"

# Adicionar repositório remoto (substitua SEU_USUARIO e SEU_REPO)
git remote add origin https://github.com/SEU_USUARIO/SEU_REPO.git

# Fazer push para GitHub
git branch -M main
git push -u origin main
```

#### Opção B: Usando Interface do GitHub

1. Acesse seu repositório no GitHub
2. Clique em "Add file" > "Upload files"
3. Selecione os arquivos:
   - `index.html`
   - `vercel.json`
   - `.gitignore`
   - `README.md`
4. Clique em "Commit changes"

### Passo 3: Fazer Deploy no Vercel

1. Acesse [vercel.com](https://vercel.com) e faça login com sua conta GitHub
2. Clique em "New Project"
3. Selecione seu repositório `dashboard-analytics`
4. Clique em "Import"
5. Na página de configuração:
   - **Framework Preset**: Deixe como "Other"
   - **Build Command**: Deixe vazio
   - **Output Directory**: Deixe como `.`
6. Clique em "Deploy"

Pronto! Seu dashboard estará online em alguns segundos!

## Configuração do Firebase

O dashboard já vem configurado com Firebase. Se quiser usar sua própria instância:

1. Abra `index.html`
2. Procure por `firebaseConfig`
3. Substitua os valores pelas suas credenciais do Firebase

## Estrutura de Dados Firebase

O dashboard espera dados no Firestore com a seguinte estrutura:

```
collections/
└── sessions
    ├── sessionId (string)
    ├── enteredAt (timestamp)
    ├── lastActivity (timestamp)
    ├── quizProgress (number)
    └── events (object)
        ├── instruction_completed (boolean)
        ├── vsl_clicked (boolean)
        ├── quiz_started (boolean)
        ├── quiz_completed (boolean)
        └── checkout_clicked (boolean)
```

## Troubleshooting

### Erro: "Cannot find module"
- Certifique-se de que todos os arquivos estão no repositório
- Verifique se o `vercel.json` está correto

### Dashboard não carrega dados
- Verifique as credenciais do Firebase
- Confirme que o Firestore tem dados na collection `sessions`
- Abra o Console do navegador (F12) para ver erros

### Erro no Vercel durante build
- Certifique-se de que não há `package.json` na raiz (para projetos estáticos puros)
- Se tiver `package.json`, deixe o `buildCommand` vazio no `vercel.json`

## Suporte

Para mais informações:
- [Documentação Vercel](https://vercel.com/docs)
- [Documentação Firebase](https://firebase.google.com/docs)
