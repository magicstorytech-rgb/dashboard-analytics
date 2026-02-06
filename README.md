# Dashboard Analytics - Protocolo TRIPE

Dashboard de analytics em tempo real com tema vermelho e preto.

## 🚀 Deploy no Vercel

### Opção 1 - Via GitHub (Recomendado)

1. Crie um repositório no GitHub
2. Faça upload destes arquivos
3. Acesse [vercel.com](https://vercel.com)
4. Clique em "Import Project"
5. Selecione seu repositório
6. Deploy automático! ✅

### Opção 2 - Via CLI

```bash
npm i -g vercel
vercel
```

### Opção 3 - Arrastar e Soltar

1. Acesse [vercel.com](https://vercel.com)
2. Arraste esta pasta para a área de upload
3. Deploy instantâneo! ✅

## 📊 Funcionalidades

- ✅ Monitoramento em tempo real
- ✅ Gráfico de acessos por horário (24h)
- ✅ Rastreamento de desconto 40% OFF
- ✅ Filtros geográficos e demográficos
- ✅ Espião de fluxo ao vivo
- ✅ Tema vermelho e preto

## 🔧 Configuração

O Firebase já está configurado. Se precisar alterar:

Edite as credenciais em `index.html`:

```javascript
const firebaseConfig = {
    apiKey: "SUA_API_KEY",
    authDomain: "SEU_DOMINIO",
    projectId: "SEU_PROJETO",
    // ...
};
```

## 📁 Estrutura

```
dashboard-project/
├── index.html      # Dashboard completo
├── vercel.json     # Config do Vercel
├── .gitignore      # Arquivos ignorados
└── README.md       # Este arquivo
```

## 🎨 Personalização

Cores principais (no CSS):
- Vermelho: `#ef4444`
- Preto: `#000000`
- Verde (sucesso): `#22c55e`
- Amarelo (desconto): `#fbbf24`

## 📝 Notas

- Dashboard atualiza a cada 30 segundos
- Gráfico mostra últimas 24 horas
- Filtros salvos no navegador
- Responsivo para mobile
