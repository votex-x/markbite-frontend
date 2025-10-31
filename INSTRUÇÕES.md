# MarkBite Frontend - Instruções de Uso

## Configuração Rápida

### 1. Abrir o Site Localmente

```bash
# Clone o repositório
git clone https://github.com/votex-x/markbite-frontend.git
cd markbite-frontend

# Abra o arquivo index.html em seu navegador
# Você pode fazer isso de várias formas:
# - Duplo clique no arquivo
# - Arraste o arquivo para o navegador
# - Use um servidor local (veja abaixo)
```

### 2. Usar um Servidor Local (Recomendado)

**Python 3:**
```bash
python -m http.server 8000
# Acesse http://localhost:8000
```

**Python 2:**
```bash
python -m SimpleHTTPServer 8000
```

**Node.js (http-server):**
```bash
npm install -g http-server
http-server
```

**PHP:**
```bash
php -S localhost:8000
```

## Configuração da API

### Passo 1: Localizar a Variável API_BASE_URL

Abra o arquivo `index.html` em um editor de texto e procure por:

```javascript
const API_BASE_URL = 'http://localhost:5000/api';
```

### Passo 2: Atualizar a URL

Se a API está em outro local, altere para:

```javascript
// Para desenvolvimento local
const API_BASE_URL = 'http://localhost:5000/api';

// Para produção (Render)
const API_BASE_URL = 'https://seu-app.onrender.com/api';

// Para qualquer outro servidor
const API_BASE_URL = 'https://seu-dominio.com/api';
```

### Passo 3: Salvar e Recarregar

1. Salve o arquivo
2. Recarregue a página no navegador (Ctrl+R ou Cmd+R)

## Usando o Site

### Buscar Produtos

1. Digite um termo de busca na caixa de entrada (ex: "notebook", "smartphone")
2. Selecione um marketplace (opcional):
   - **Todos** - Busca em todos os marketplaces
   - **Mercado Livre** - Apenas Mercado Livre
   - **Shopee** - Apenas Shopee
   - **AliExpress** - Apenas AliExpress
3. Clique em "Buscar" ou pressione Enter

### Ordenar Resultados

Use o filtro "Ordenar por":
- **Menor Preço** - Produtos mais baratos primeiro
- **Maior Preço** - Produtos mais caros primeiro
- **Relevância** - Ordem padrão

### Comparar Preços

A seção "Comparação de Preços" mostra:
- **Melhor preço** - O produto mais barato encontrado
- **Marketplace** - Onde encontrar o melhor preço
- **Top 3 produtos** de cada marketplace

### Ver Estatísticas

Após uma busca, você verá:
- **Produtos encontrados** - Total de resultados
- **Marketplaces** - Quantos marketplaces têm o produto
- **Menor preço** - Preço mínimo encontrado
- **Maior preço** - Preço máximo encontrado
- **Preço médio** - Média de preços

## Troubleshooting

### "API não está respondendo"

**Solução:**
1. Certifique-se de que a API está rodando
2. Verifique a URL em `API_BASE_URL`
3. Abra o console (F12) e procure por erros CORS

### "Nenhum produto encontrado"

**Solução:**
1. Tente um termo de busca diferente
2. Verifique a ortografia
3. Alguns marketplaces podem estar bloqueando o scraping temporariamente

### "Erro 500 na API"

**Solução:**
1. Verifique os logs da API
2. Reinicie a API
3. Certifique-se de que todas as dependências estão instaladas

### "Página em branco"

**Solução:**
1. Verifique se o arquivo `index.html` está intacto
2. Abra o console (F12) e procure por erros de JavaScript
3. Tente limpar o cache do navegador (Ctrl+Shift+Delete)

## Deploy em Produção

### Netlify

```bash
# 1. Faça push para GitHub
git push origin main

# 2. Acesse https://netlify.com
# 3. Clique em "New site from Git"
# 4. Selecione o repositório
# 5. Deploy automático
```

### Vercel

```bash
# 1. Instale a CLI do Vercel
npm install -g vercel

# 2. Deploy
vercel

# 3. Siga as instruções
```

### GitHub Pages

```bash
# 1. Vá para Settings → Pages
# 2. Selecione "Deploy from a branch"
# 3. Escolha a branch main
# 4. Seu site estará em https://seu-usuario.github.io/markbite-frontend
```

## Variáveis de Ambiente

Se você quiser usar variáveis de ambiente, crie um arquivo `.env`:

```
VITE_API_URL=https://seu-api.onrender.com/api
```

Depois atualize o `index.html`:

```javascript
const API_BASE_URL = process.env.VITE_API_URL || 'http://localhost:5000/api';
```

## Performance

### Dicas para Melhor Performance

1. **Use um servidor local** em vez de abrir o arquivo diretamente
2. **Atualize o navegador** regularmente
3. **Limpe o cache** se tiver problemas
4. **Use um CDN** para servir o arquivo em produção

### Otimizações Implementadas

- ✅ CSS inline para evitar requisições extras
- ✅ JavaScript otimizado
- ✅ Imagens em formato otimizado
- ✅ Lazy loading de conteúdo

## Segurança

### Considerações de Segurança

1. **CORS**: A API deve ter CORS configurado corretamente
2. **HTTPS**: Use HTTPS em produção
3. **Validação**: Sempre valide dados no servidor
4. **Rate Limiting**: Implemente rate limiting na API

## Suporte

Para dúvidas ou problemas:

1. Abra uma issue no GitHub
2. Verifique a documentação da API
3. Consulte o console do navegador (F12)

## Próximas Melhorias

- [ ] Modo escuro
- [ ] Histórico de buscas
- [ ] Favoritos
- [ ] Alertas de preço
- [ ] PWA (offline support)
- [ ] Integração com APIs oficiais

## Licença

MIT
