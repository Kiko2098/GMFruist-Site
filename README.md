# GM Fruits — Landing Page

Site institucional da **GM Fruits** — Origen Quality Trust.

## Estrutura de ficheiros

```
GMFruits Site/
├── index.html        # Página principal
├── css/
│   └── style.css     # Todos os estilos (custom properties, componentes, responsive)
├── js/
│   └── script.js     # Header scroll, menu mobile, reveal, contadores, formulário
└── images/           # (adicionar imagens próprias aqui)
```

## Executar localmente

Abrir o `index.html` diretamente no browser **ou** usar um servidor local
(recomendado para evitar restrições CORS nas imagens):

```bash
# Com Python 3
cd "GMFruits Site"
python3 -m http.server 8080
# Abrir http://localhost:8080
```

Alternativas: extensão **Live Server** no VS Code, ou `npx serve .`

## Deploy no Netlify

1. Arrastar a pasta `GMFruits Site` para [app.netlify.com/drop](https://app.netlify.com/drop)  
2. O site fica online imediatamente com URL gerado automaticamente.

Para deploy contínuo via Git:
1. Criar repositório no GitHub e fazer push da pasta
2. Em Netlify → **Add new site → Import from Git**
3. Build command: *(deixar vazio)* · Publish directory: `.`

## Deploy no Vercel

```bash
npm i -g vercel
cd "GMFruits Site"
vercel
```

Seguir as instruções no terminal. Framework preset: **Other**.

## Personalizar conteúdo

| O que mudar | Onde |
|---|---|
| Textos / conteúdo | `index.html` — procurar a secção pretendida |
| Cores da marca | `css/style.css` → bloco `:root { }` no topo |
| Fontes | `index.html` `<link>` Google Fonts + variáveis `--font-*` no CSS |
| Imagens | Substituir URLs Unsplash por caminhos locais em `images/` |
| Email do formulário | `js/script.js` → substituir `setTimeout` por chamada real a API/serviço |
| Mapa | Gerar novo embed em maps.google.com e substituir o `src` do `<iframe>` |

## Funcionalidades incluídas

- Header transparente → sólido no scroll
- Menu hamburger animado (mobile)
- Smooth scroll para todas as secções
- Highlight do link ativo na navegação
- Animações fade-in/reveal ao scroll (Intersection Observer)
- Contadores animados nos números
- Validação do formulário de contacto
- Botão "voltar ao topo"
- Totalmente responsivo (mobile-first)

## Sugestões de melhorias futuras

- [ ] Integrar formulário com Netlify Forms, Formspree ou EmailJS
- [ ] Adicionar galeria de produtos com lightbox
- [ ] Secção de blog / notícias
- [ ] Animação parallax no hero
- [ ] Versão multilingue (PT / EN / ES)
- [ ] Cookie consent banner (RGPD)
- [ ] Google Analytics / Meta Pixel
- [ ] PWA manifest para instalação mobile
