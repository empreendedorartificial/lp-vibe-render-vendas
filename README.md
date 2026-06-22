# LP Vibe Render — Página de vendas oficial

Página de vendas do minicurso Vibe Render (Academy). HTML único + assets, deploy via GitHub + Cloudflare Pages.

## Estrutura
- `index.html` — página completa (CSS e JS inline)
- `assets/img/` — renders, posters, foto do Montani, avatares dos depoimentos (`dep/`)
- `assets/video/` — vídeos comprimidos para web (H.264, mudo, loop, <7MB cada)

## Pontos editáveis frequentes
- **Data da barra do topo**: gerada automática via JS (dia vigente). Não precisa editar.
- **Preços**: oferta em `R$ 197` à vista, ancoragem `R$ 497`, `12x de R$ 19,43`. Ficam na barra do topo, na seção de oferta e na barra fixa mobile.
- **Link de checkout** (todos os botões de compra): `https://pay.hotmart.com/E105428912P?checkoutMode=10`
- **Pixel Meta**: `2428536680685666` (PageView) no `<head>`.
- **Aula liberada**: player VTurb `vid-6a2b930d7f684d974fa50130` dentro de `#aulaEmbed` (seção pós-depoimentos).

## Mídia
Vídeos comprimidos com ffmpeg (lado maior 1000px, CRF 28, sem áudio, faststart) e carregados sob demanda (lazy + autoplay quando visível). Posters em `assets/img/poster-*.jpg`.

## Depoimentos
Replicam o formato da página do workshop (marquee 2 fileiras, cards review + WhatsApp). Dados no bloco `<script>` no fim do `index.html`. Avatares reais em `assets/img/dep/`.

## Deploy
Repositório git conectado ao Cloudflare Pages. Build vazio (HTML estático), output `/`. Alteração → `git commit` + `git push` → deploy automático em ~30s.

Arquivos de trabalho (`_work/`, `_tools/`, `_draft_package/`, `_materiais/`, `base_v3.html`) estão no `.gitignore` e não vão pro deploy.
