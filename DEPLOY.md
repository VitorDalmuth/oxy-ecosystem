# 🚀 Guia de Deploy - Proposta OXY EcoSystem

## Passo a passo para colocar no ar

### 1️⃣ PREPARAR REPOSITÓRIO GIT

```bash
# Navegar para a pasta do projeto
cd proposta-oxy-vercel

# Inicializar git
git init

# Adicionar todos os arquivos
git add .

# Primeiro commit
git commit -m "feat: proposta comercial OXY EcoSystem - 2STEP MÍDIA"

# Conectar ao GitHub (substitua pela sua URL)
git remote add origin https://github.com/SEU_USUARIO/proposta-oxy-ecosystem.git

# Enviar para o GitHub
git push -u origin main
```

### 2️⃣ DEPLOY NO VERCEL

**Opção A: Interface Web (Recomendado)**
1. Acesse [vercel.com](https://vercel.com)
2. Conecte sua conta GitHub
3. Clique em "New Project"
4. Selecione o repositório "proposta-oxy-ecosystem"
5. Clique em "Deploy"

**Opção B: Vercel CLI**
```bash
# Instalar Vercel CLI
npm i -g vercel

# Fazer login
vercel login

# Deploy
vercel --prod
```

**Opção C: Drag & Drop**
1. Comprima a pasta em ZIP
2. Acesse [vercel.com](https://vercel.com)
3. Arraste o ZIP diretamente no dashboard

### 3️⃣ CONFIGURAÇÕES IMPORTANTES

**Configurações no Vercel:**
- Build Command: `(deixar vazio)`
- Output Directory: `(deixar vazio)`
- Install Command: `(deixar vazio)`
- Development Command: `npx serve .`

**Environment Variables:**
Não são necessárias para este projeto.

### 4️⃣ DOMAIN PERSONALIZADO (OPCIONAL)

1. No dashboard do Vercel, vá em "Domains"
2. Adicione seu domínio personalizado
3. Configure os DNS conforme instruções

### 5️⃣ OTIMIZAÇÕES PÓS-DEPLOY

**Performance:**
- ✅ CSS minificado
- ✅ Fontes otimizadas (Google Fonts)
- ✅ JavaScript vanilla (sem frameworks)
- ✅ Imagens em base64 (sem requests externos)

**SEO:**
- ✅ Meta tags configuradas
- ✅ Título e descrição otimizados
- ✅ Estrutura semântica HTML5

**Analytics (opcional):**
Para adicionar Google Analytics, insira antes de `</head>`:
```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_TRACKING_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_TRACKING_ID');
</script>
```

### 6️⃣ MANUTENÇÃO

**Atualizações:**
```bash
# Fazer alterações nos arquivos
git add .
git commit -m "update: descrição da mudança"
git push

# Deploy automático será disparado
```

**Monitoramento:**
- Dashboard Vercel: analytics integrado
- Logs de deploy e runtime
- Métricas de performance

### 🎯 RESULTADO FINAL

Após o deploy, você terá:
- ✅ Site responsivo funcionando
- ✅ HTTPS automático
- ✅ CDN global
- ✅ Deploy automático a cada push
- ✅ URL amigável (.vercel.app)

**URL de exemplo:** 
`https://proposta-oxy-ecosystem.vercel.app`

---

## 🆘 Problemas Comuns

**Deploy falha:**
- Verificar se todos os arquivos estão no repositório
- Confirmar se não há erros no HTML/CSS/JS

**Site não carrega:**
- Verificar console do browser (F12)
- Confirmar se fontes Google estão carregando

**Animações não funcionam:**
- Verificar se JavaScript está habilitado
- Testar em modo incógnito

---

**Suporte:** 
- Documentação Vercel: [vercel.com/docs](https://vercel.com/docs)
- Este README.md contém todas as informações técnicas
