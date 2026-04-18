# Vestibular ITA — Landing Page

Landing page institucional para o processo seletivo do ITA (Instituto Tecnológico de Aeronáutica), desenvolvida como projeto prático de aprendizado de HTML e CSS.

## Estrutura do projeto

```
.
├── index.html      # Estrutura e conteúdo da página
└── styles.css      # Estilos, layout e animações
```

## Seções da página

| Seção | Descrição |
|---|---|
| **Navbar** | Barra de navegação sticky com logo e links âncora |
| **Hero** | Apresentação principal com título, estatísticas e CTAs |
| **Sobre** | Cards informativos sobre o ITA |
| **Cronograma** | Linha do tempo com as etapas do vestibular 2027 |
| **Fases** | Detalhamento das duas fases do processo seletivo |
| **CTA Final** | Chamada para inscrição com link ao site oficial |
| **Footer** | Informações institucionais e disclaimer |

## Tecnologias

- **HTML5** semântico (uso de `<header>`, `<nav>`, `<section>`, `<footer>`)
- **CSS puro** — sem frameworks ou dependências externas
- [Google Fonts](https://fonts.google.com): `Syne` (títulos) e `IBM Plex Mono` (detalhes técnicos)

## Conceitos CSS aplicados

### Design tokens
Todas as cores, fontes e espaçamentos são definidos como **custom properties** em `:root`, facilitando manutenção e consistência visual:

```css
:root {
  --color-accent:  #00c8ff;
  --font-display:  'Syne', sans-serif;
  --space-lg:      4rem;
}
```

### Componentes com BEM
Os botões seguem a metodologia **BEM** (Block, Element, Modifier): uma classe base `.btn` com variantes `.btn--primary`, `.btn--outline` e `.btn--ghost`.

### Layout
- **Flexbox** — navbar, hero, footer, cards internos
- **CSS Grid** — grade de cards (`cards-grid`) e fases (`phases-grid`)
- **`position: sticky`** — navbar fixa no topo durante o scroll

### Efeitos visuais
- `backdrop-filter: blur()` — efeito de vidro fosco na navbar
- `filter: blur()` — círculos de fundo desfocados no hero
- Pseudo-elementos `::before` — linha e pontos da timeline sem HTML extra
- `@keyframes` — animações `fadeUp`, `pulse` e `pulse-dot`

### Responsividade
Media query em `max-width: 768px` adapta o layout para mobile:
- Grid de 3 colunas → 1 coluna
- Timeline reposicionada
- Links da navbar ocultados (mantém apenas o botão de inscrição)

## Paleta de cores

| Variável | Hex | Uso |
|---|---|---|
| `--color-bg` | `#0a0c10` | Fundo geral |
| `--color-surface` | `#111520` | Cards e seções escuras |
| `--color-accent` | `#00c8ff` | Destaque azul elétrico |
| `--color-accent-2` | `#0056ff` | Gradientes |
| `--color-text` | `#e8edf5` | Texto principal |
| `--color-muted` | `#6b7a99` | Texto secundário |

## Como rodar

Nenhuma dependência ou build step necessário. Basta abrir o `index.html` no navegador:

```bash
# Com VS Code + extensão Live Server
# Clique com botão direito em index.html → "Open with Live Server"

# Ou via terminal (Python)
python3 -m http.server 8080
# Acesse http://localhost:8080
```

## Aviso

Esta é uma **página de demonstração** desenvolvida para fins educacionais. Para informações oficiais sobre o vestibular, acesse [vestibular.ita.br](https://www.vestibular.ita.br).
