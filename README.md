# MarkBite - Frontend

Frontend em HTML, CSS e JavaScript puro para o agregador de preços MarkBite.

## Sobre

MarkBite é um agregador de preços que permite comparar produtos de múltiplos marketplaces brasileiros (Mercado Livre, Shopee, AliExpress) em um único lugar.

## Funcionalidades

- 🔍 Busca de produtos em tempo real
- 💰 Comparação de preços entre marketplaces
- 📊 Estatísticas de preços (mínimo, máximo, médio)
- 🎯 Filtros por marketplace
- 📱 Design responsivo e mobile-friendly
- ⚡ Interface rápida e intuitiva

## Como Usar

### Localmente

1. Clone o repositório:
```bash
git clone https://github.com/votex-x/markbite-frontend.git
cd markbite-frontend
```

2. Abra o arquivo `index.html` em seu navegador

3. Certifique-se de que a API está rodando em `http://localhost:5000`

### Em Produção

1. Atualize a variável `API_BASE_URL` no arquivo `index.html`:
```javascript
const API_BASE_URL = 'https://sua-api.onrender.com/api';
```

2. Faça o deploy em qualquer servidor web ou plataforma de hosting

## Estrutura

```
markbite-frontend/
├── index.html          # Página principal (HTML + CSS + JavaScript)
├── README.md           # Este arquivo
└── .gitignore
```

## Requisitos

- Navegador moderno (Chrome, Firefox, Safari, Edge)
- Conexão com a internet
- API MarkBite rodando (ver repositório markbite-api)

## Deploy

### Opção 1: Netlify (Recomendado)

1. Faça push do código para GitHub
2. Acesse https://netlify.com
3. Clique em "New site from Git"
4. Selecione o repositório
5. Deploy automático

### Opção 2: Vercel

1. Acesse https://vercel.com
2. Importe o repositório GitHub
3. Deploy automático

### Opção 3: GitHub Pages

1. Vá para Settings → Pages
2. Selecione "Deploy from a branch"
3. Escolha a branch `main`
4. Seu site estará em `https://seu-usuario.github.io/markbite-frontend`

### Opção 4: Servidor Próprio

Copie o arquivo `index.html` para qualquer servidor web (Apache, Nginx, etc.)

## Configuração da API

Antes de usar, certifique-se de que:

1. A API MarkBite está rodando
2. A URL da API está correta em `API_BASE_URL`
3. CORS está habilitado na API (já configurado por padrão)

## Endpoints da API Esperados

- `GET /api/health` - Health check
- `GET /api/search?q=<termo>&marketplace=<marketplace>` - Buscar produtos
- `GET /api/compare?q=<termo>` - Comparar preços

## Tecnologias

- HTML5
- CSS3 (com Flexbox e Grid)
- JavaScript ES6+
- Fetch API

## Compatibilidade

- ✅ Chrome/Chromium
- ✅ Firefox
- ✅ Safari
- ✅ Edge
- ✅ Mobile browsers

## Melhorias Futuras

- [ ] Cache local de resultados
- [ ] Histórico de buscas
- [ ] Modo escuro
- [ ] Alertas de preço
- [ ] Favoritos e listas de desejos
- [ ] PWA (Progressive Web App)

## Licença

MIT

## Suporte

Para dúvidas ou problemas, abra uma issue no repositório.

## Repositórios Relacionados

- [MarkBite API](https://github.com/votex-x/markbite-api) - Backend com web scraping
