# trilo-web

Site institucional do Trilo. Contém landing page, política de privacidade, termos de uso e suporte.

## Arquivos

- `index.html` — landing page (raiz)
- `privacy.html` — política de privacidade
- `terms.html` — termos de uso
- `support.html` — FAQ e contato
- `style.css` — estilo compartilhado

## Hospedagem

As páginas são HTML estático puro — não precisam de build, framework ou servidor. Podem ser hospedadas em:

- **GitHub Pages** (free) — basta apontar o GitHub Pages para esta pasta
- **Vercel / Netlify** (free) — drag & drop ou conectar ao repo
- **Cloudflare Pages** (free)
- Qualquer servidor estático

## Após publicar

Atualize as 3 URLs no app iOS em `SettingsViewModel.swift`:

```swift
let privacyPolicyURL = URL(string: "SUA-URL-AQUI/privacy.html")!
let termsOfUseURL = URL(string: "SUA-URL-AQUI/terms.html")!
// Adicione também o supportURL se for criar
```

## Customização

- Cor principal (verde-teal): definida em `style.css` na variável `--color-accent`
- Email de contato: `denilson100@gmail.com` (substituir nos 4 arquivos HTML se mudar)
- Suporta dark mode automaticamente via `@media (prefers-color-scheme: dark)`
- Layout responsivo (mobile + desktop)

## Identidade visual

O logo é construído em HTML/CSS puro (3 retângulos brancos ascendentes em fundo verde), espelhando o ícone do app iOS. Sem dependência de arquivos de imagem.
