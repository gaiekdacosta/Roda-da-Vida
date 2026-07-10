# 🎡 Roda da Vida

Aplicação web para o exercício clássico da **Roda da Vida**: avalie as 12 áreas
da sua vida com notas de 0 a 10, visualize seu equilíbrio em um gráfico radial
e exporte o resultado como imagem.

**100% frontend** — um único arquivo, sem build, sem dependências, sem login e
sem envio de dados a servidores.

## Como usar

Abra o arquivo [`index.html`](index.html) em qualquer navegador moderno.
Pronto — não precisa instalar nada.

```bash
# opcional: servir localmente
npx serve .
```

## Funcionalidades

- **Roda interativa** — toque ou arraste em uma fatia para dar a nota, ou use
  os controles deslizantes; a média aparece no centro
- **12 áreas em 4 quadrantes** (Pessoal, Profissional, Relacionamentos,
  Qualidade de Vida), com nomes editáveis (ícone de lápis)
- **Insights automáticos** — ponto forte e área que merece atenção
- **Exportar PNG** — imagem 1080×1350 (proporção ideal para redes sociais) com
  roda, legenda, notas e data
- **Compartilhar** — via Web Share API (aparece em dispositivos compatíveis,
  ex.: celulares), com **legenda personalizada** que inclui a média, o ponto
  forte, a área que merece atenção e um convite com o link do app
- **Prévia de link profissional** — meta tags Open Graph/Twitter Card + imagem
  `og-image.png` fazem o link exibir um cartão bonito ao ser compartilhado
  (WhatsApp, LinkedIn, X, etc.)
- **Salvamento automático** — suas notas ficam no `localStorage` do navegador
- **Tema claro/escuro** — segue o sistema, com alternância manual
- **Mobile-first e acessível** — sliders nativos com rótulos, paleta validada
  para daltonismo, suporte a `prefers-reduced-motion`

## Estrutura

| Arquivo | Descrição |
|---|---|
| `index.html` | Aplicação completa (HTML + CSS + JS embutidos) |
| `og-image.png` | Imagem de prévia (1200×630) para os cartões de link |

> A prévia de link só é lida por WhatsApp/redes quando o site está **publicado**
> (URL `http`/`https`). Abrindo o arquivo local (`file://`), o compartilhamento
> ainda funciona com a imagem exportada e a legenda personalizada.

## Personalização rápida

- **Áreas padrão**: edite o array `DEFAULT_AREAS` em `index.html`
- **Cores dos quadrantes**: variáveis CSS `--q0` a `--q3` (claro e escuro)
- **Textos**: todo o conteúdo está em português no próprio HTML
