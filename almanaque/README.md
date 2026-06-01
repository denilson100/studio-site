# Almanaque — Site oficial

Site institucional do app **Almanaque do Boleiro**, hospedado no GitHub Pages.

## Estrutura

```
almanaque-site/
├── index.html          # Página inicial (marketing)
├── privacy.html        # Política de Privacidade
├── support.html        # Suporte e FAQ
├── style.css           # Estilos compartilhados
└── README.md           # Este arquivo
```

## Tecnologia

- **HTML5 + CSS3 puro** — sem build, sem dependências, sem JS framework
- **Fontes Google:** Bebas Neue (display), Playfair Display (serif), JetBrains Mono (mono)
- **Compatibilidade:** todos os navegadores modernos + iOS Safari

## Deploy no GitHub Pages

### Setup inicial

1. Criar repositório público no GitHub (sugestão: `almanaque-site` ou `almanaque-app`)
2. Subir todos os arquivos para a branch `main`:
   ```bash
   cd almanaque-site
   git init
   git add .
   git commit -m "Initial commit: site oficial do Almanaque"
   git branch -M main
   git remote add origin https://github.com/<seu-usuario>/almanaque-site.git
   git push -u origin main
   ```
3. No GitHub: **Settings** → **Pages**
4. **Source:** `Deploy from a branch`
5. **Branch:** `main`, pasta `/ (root)`
6. **Save**

GitHub publica em 1-2 minutos. URL final:

```
https://<seu-usuario>.github.io/almanaque-site/
```

### URLs específicas

- Página inicial (marketing): `https://<seu-usuario>.github.io/almanaque-site/`
- Suporte: `https://<seu-usuario>.github.io/almanaque-site/support.html`
- Privacidade: `https://<seu-usuario>.github.io/almanaque-site/privacy.html`

### Domínio personalizado (opcional)

Se você comprar `almanaqueapp.com.br` ou similar:

1. Criar arquivo `CNAME` na raiz do repo com o domínio:
   ```
   almanaqueapp.com.br
   ```
2. Configurar DNS no provedor do domínio:
   - Tipo `CNAME`, nome `www`, valor `<seu-usuario>.github.io`
   - Tipo `A`, nome `@`, valores:
     - `185.199.108.153`
     - `185.199.109.153`
     - `185.199.110.153`
     - `185.199.111.153`
3. No GitHub Pages, habilitar **Enforce HTTPS**

## Onde usar cada URL

| URL | Onde colocar |
|---|---|
| `https://.../` | App Store Connect > Marketing URL |
| `https://.../support.html` | App Store Connect > Support URL |
| `https://.../privacy.html` | App Store Connect > Privacy Policy URL |
| `https://.../privacy.html` | `AboutView.swift` no app (link de Política) |
| `https://.../support.html` | `AboutView.swift` no app (link de Suporte) |

## Atualizações futuras

Pra atualizar conteúdo, edite os HTMLs e dê push pra branch `main`. GitHub Pages atualiza automaticamente em 1-2 minutos.

## Manutenção

- **Atualizar data:** quando fizer mudanças relevantes na Política, atualizar a string "maio de 2026" em `privacy.html`
- **Atualizar FAQ:** adicionar/remover blocos `<details class="faq-item">` em `support.html`
- **Mudar e-mail:** se o e-mail mudar, substituir todas as ocorrências de `denilson.monteiro.dev@gmail.com` nos 3 HTMLs

## Identidade visual

- **Paleta:** alinhada com o Design System v2 do app (sépia, verde gramado, mostarda dourada, vermelho almanaque)
- **Tipografia:** Bebas Neue (display) imita o varsity bold condensed do app
- **Vibe:** vintage editorial, evocando capas de revistas esportivas dos anos 70/80

---

**Versão:** 1.0
