# Site — Dênia Virgínia Fonseca, Psicóloga Clínica

Página única em HTML/CSS estático, pronta para GitHub Pages. Layout e textos seguem o modelo visual de referência (imagem do site completo); dados, SEO e o teste de TDAH vêm de `ESPECIFICACOES_SITE_DENIA.md` (v1.0, 20/10/2026).

O "Blog" e a seção "Artigos recentes" do modelo ficaram de fora até existirem artigos publicados, assim como os links "Saiba mais" e "Conheça minha trajetória", que ainda não têm páginas de destino.

## Estrutura

```
index.html        página inicial
styles.css        estilos (paleta da marca, contraste AA)
robots.txt        só tem efeito na raiz de um domínio (ex.: domínio próprio)
sitemap.xml       submeter no Google Search Console após publicar
assets/           imagens — manter SEMPRE ao lado do index.html
mapa/             página anterior do MAPA de Identidade Neuroemocional, preservada sem alterações
```

Em `assets/`:

- Originais entregues pela profissional: `hero.png`, `sobre.png`, `leitura.png`, `online.png` (não usada no layout atual), `logo.jpg`, `simbolo.jpg`.
- Versões usadas no site: `*-640.webp`, `*-1080.webp` e `*-1080.jpg` (fallback), `logo-cabecalho.webp/.png` (logo original recortado, com fundo transparente), `simbolo-marca.webp/.png` (símbolo transparente, decorativo em "Sobre mim"), `favicon-32.png`, `favicon-192.png`, `apple-touch-icon.png` e `og-image.jpg` (1200×630, imagem de compartilhamento).

Fontes (Google Fonts): EB Garamond nos títulos, Manrope no texto e Caveat nos trechos manuscritos. A Cormorant Garamond foi descartada porque desloca o circunflexo ("você", "Dênia"). Ícones: Lucide (licença ISC), embutidos como SVG no `index.html`.

Todos os caminhos são relativos, então o site funciona tanto em `/lead_page/` quanto na raiz de um domínio. Atenção a maiúsculas/minúsculas nos nomes de arquivo: o GitHub Pages diferencia.

## Visualizar localmente

Abra o `index.html` no navegador sem tirá-lo da pasta (as imagens estão em `assets/`), ou sirva a pasta:

```bash
python -m http.server 8000
```

## Antes de publicar em produção

1. Revisar a prévia com a profissional (textos, dados de atendimento e conformidade ética). Os textos do modelo visual diferem da especificação aprovada: confirmar em especial "Talvez você seja neurodivergente" e "Diagnóstico tardio", já que a especificação pede evitar alegações diagnósticas.
2. Confirmar a URL definitiva. Hoje `og:image`, `sitemap.xml` e `robots.txt` apontam para `https://deniavfonseca.github.io/lead_page/`; se mudar (ex.: domínio próprio), atualizar os três e ativar `canonical` e `og:url` (comentados no `<head>` do `index.html`).
3. Revisar no app do teste (https://tdahfeminio.up.railway.app/) a coleta de dados, o consentimento, a privacidade e a interpretação dos resultados.
4. Clicar em todos os botões de WhatsApp e no link do teste.
5. Após publicar: submeter o `sitemap.xml` no Search Console e medir no PageSpeed Insights.
6. Adicionar Política de Privacidade (e o link no rodapé) caso entre analytics, formulários ou cookies. Os botões já têm `data-cta` para facilitar o rastreamento de cliques.
