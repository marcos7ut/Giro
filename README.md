# giro.

**Painéis de vendas para lojistas.** O Giro transforma as planilhas que a loja já usa em um painel no celular: o que encalhou, o que vai faltar, quem vende mais e qual dia dá lucro.

🔗 Site: https://marcos7ut.github.io/Giro/
📱 App (teste grátis por 7 dias): https://marcos7ut.github.io/Giro/app/

---

## Estrutura

| Arquivo | O que é |
|---|---|
| `index.html` | Página de vendas (HTML, CSS e JS num arquivo só, sem dependências) |
| `app/index.html` | Abre o Giro App (hospedado no Streamlit Community Cloud) em tela cheia, com tela de carregamento |
| `privacidade.html` | Política de privacidade (LGPD) e termos de uso |
| `404.html` | Página de "não encontrado" do GitHub Pages |
| `sitemap.xml` | Mapa do site para o Google |
| `manifest.webmanifest`, `app/manifest.webmanifest` | Permitem "instalar" o site e o app na tela inicial do celular |
| `giro-*.webp` | Fotos da seção "Feito para o seu ramo" |
| `og-image.jpg`, `og-app.jpg` | Imagens de pré-visualização ao compartilhar o link (1200×630) |

## Configuração rápida

- **Número do WhatsApp:** constante `WHATS` no início do `<script>` de `index.html`. Os links são montados por JavaScript para o número não ficar exposto no HTML.
- **Endereço do app:** constante `APP` em `app/index.html`.
- **Preços:** seção `#planos` de `index.html` **e** o bloco `application/ld+json` no `<head>` (dados para o Google). Mantenha os dois iguais.
- **Perguntas frequentes:** seção `#duvidas` e o `FAQPage` no mesmo bloco `ld+json`.
- **Seções do menu:** o destaque do item ativo segue a ordem dos links de `#navLinks`; basta o `href` apontar para o `id` da seção.

## Publicação

O site é servido pelo **GitHub Pages** direto da branch principal (Settings → Pages). Não há build: o que está no repositório é o que vai ao ar.

Depois de publicar uma mudança, vale conferir:

1. [PageSpeed Insights](https://pagespeed.web.dev/) — desempenho e acessibilidade no celular.
2. [Teste de resultados avançados do Google](https://search.google.com/test/rich-results) — dados estruturados.
3. [Depurador do Facebook](https://developers.facebook.com/tools/debug/) — pré-visualização no WhatsApp/Instagram (use "Scrape again" depois de trocar a `og-image`).

## Privacidade

O site não usa cookies, analytics nem rastreadores de publicidade. A política completa está em [`privacidade.html`](privacidade.html).

---

Feito por **Marcos Lima** (Taboão da Serra, SP) e **Fernando Henrique** (Sorocaba, SP).
