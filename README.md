# OCTA — Link in bio (Otávio Designer)

Página de links pra bio do Instagram. Site estático, sem build — é só HTML/CSS/JS puro.

## Estrutura
```
.
├── index.html          # a página inteira (tudo aqui)
└── assets/
    ├── otavio.jpg      # foto de perfil
    └── favicon.svg     # ícone da aba (símbolo OCTA)
```

## Rodar local
Abra o `index.html` no navegador. (Ou sirva a pasta: `python3 -m http.server` e acesse `http://localhost:8000`.)

## Publicar no Vercel

**1. Subir pro GitHub** (crie um repo vazio em https://github.com/new — sem README):
```bash
git remote add origin https://github.com/SEU-USUARIO/octa-bio.git
git branch -M main
git push -u origin main
```

**2. Conectar no Vercel:**
- Entre em https://vercel.com → **Add New… → Project → Import** o repositório.
- **Framework Preset:** `Other`  ·  **Build Command:** (vazio)  ·  **Output Directory:** (vazio / raiz).
- Clique em **Deploy**. Pronto — a URL sai em segundos.
- Pra domínio próprio: Project → **Settings → Domains**.

> Não precisa de build nem de configuração extra: é estático.

## Antes de publicar — trocar os placeholders
No `index.html`, procure e substitua pelas URLs reais:

| Placeholder | Onde aparece |
|---|---|
| `#TROCAR-URL-DA-AGENCIA` | botão Agência OCTA 360º |
| `#TROCAR-URL-DO-SITE` | botão Site + logo do rodapé |
| `#TROCAR-URL-DO-BEHANCE` | botão Behance + ícone social |
| `#TROCAR-URL-DO-INSTAGRAM` | ícone do Instagram |
| `#TROCAR-EMAIL` | ícone de email (use `mailto:seu@email.com`) |

## Trocar a arte de cada botão
Cada botão tem uma linha comentada. Descomente e aponte pro seu arquivo em `assets/`:
```html
<!-- <img src="assets/arte-agencia.jpg" alt=""> -->
```
vira
```html
<img src="assets/arte-agencia.jpg" alt="">
```
