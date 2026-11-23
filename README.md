# Biblioteca-Digital-UniFECAF
trabalho de design web sobre a biblioteca da UNIFECAF
# Biblioteca Digital UniFECAF

Primeira versão do site da **Biblioteca Digital UniFECAF**, feita apenas com **HTML e CSS** a partir de um protótipo de baixa fidelidade fornecido pela instituição.

🔗 **Site publicado:** https://predobrito.github.io/Biblioteca-Digital-UniFECAF/

---

## Sobre o projeto

Este projeto foi desenvolvido para a disciplina **Design Web** do curso de Ciência da Computação do Centro Universitário UniFECAF.

O desafio era responder a uma pergunta:

> Como transformar um protótipo de baixa fidelidade em uma interface web moderna, responsiva e alinhada à identidade visual da UniFECAF?

O site mantém as seções e a organização do protótipo, e as decisões de cores, tipografia, imagens e textos foram definidas por mim.

## Seções da página

| Seção | O que mostra |
|---|---|
| **Menu** | Barra fixa no topo com Biblioteca, Livros, Unidades e Contato |
| **Banner** | Título, texto de apoio, botão "Explorar livros" e ilustração em SVG |
| **Sobre a nossa biblioteca** | Textos, uma foto e uma galeria com 4 imagens |
| **Faixa ilustrada** | Faixa de largura total com estantes de livros |
| **Nossos livros** | 6 cards (categoria, título, capa, descrição e botão "Saiba mais") |
| **As unidades e polos** | 3 blocos com imagem e texto, alternando o lado da imagem |
| **Contato** | Chamada para a página oficial da biblioteca e card com ilustração |
| **Rodapé** | Marca e link "Voltar ao topo" |

## Tecnologias

- **HTML5** semântico (`header`, `nav`, `main`, `section`, `article`, `figure`, `footer`)
- **CSS3** em arquivo separado, com variáveis (`:root`), Grid, Flexbox e *media queries*
- **Google Fonts:** Montserrat (títulos) e Nunito Sans (texto)

Não foram usados construtores de site, templates prontos, frameworks CSS nem JavaScript.

## Identidade visual

A paleta parte do azul e do verde da UniFECAF. Cada cor tem uma função e está declarada como variável no início do CSS.

| Cor | Código | Uso |
|---|---|---|
| Azul-marinho profundo | `#101a3c` | Títulos e fundo da seção Contato |
| Azul-marinho | `#142b62` | Marca, links e faixa de estantes |
| Azul médio | `#31539a` | Detalhes e ilustrações |
| Verde escuro | `#008653` | Botões principais, rótulos e destaques em texto |
| Verde vivo | `#00a96b` | Somente ilustrações e detalhes gráficos |
| Grafite | `#202536` | Texto corrido |
| Cinza-azulado | `#646b7c` | Textos secundários |
| Névoa | `#f4f6fa` | Fundo da seção de livros e do banner |

## Responsividade

O layout foi testado em computador (1366 px), tablet (820 px) e smartphone (390 px), sem rolagem horizontal, texto cortado ou imagem distorcida.

| Largura | O que muda |
|---|---|
| Acima de 900 px | Layout completo: 3 colunas em "Sobre", 3 colunas nos livros, unidades em zigue-zague |
| Até 900 px | "Sobre" e livros em 2 colunas |
| Até 650 px | Menu em linha própria, com os 4 links em grade; seções em coluna única |
| Até 360 px | Ajustes finos de margem, fonte e altura das capas |

Técnicas usadas: `meta viewport`, `min()` no container, `minmax(0, 1fr)` nas colunas do Grid, `clamp()` no título principal e `object-fit` nas imagens.

## Acessibilidade

- `lang="pt-BR"` no HTML
- Estrutura semântica e hierarquia de títulos (`h1` → `h2` → `h3`)
- Texto alternativo nas imagens de conteúdo; ilustrações decorativas com `aria-hidden`
- `aria-label` na navegação e na marca
- Foco visível para navegação por teclado (`:focus-visible`)
- Pares de cores de texto com contraste mínimo de 4,5:1 (exceto os rótulos pequenos em verde escuro sobre fundos acinzentados, com cerca de 4,3:1)
- Links externos com `rel="noopener"`

## Estrutura de arquivos

```
Biblioteca-Digital-UniFECAF/
├── index.html
├── LEIA-ME.txt
├── css/
│   └── style.css
└── assets/
    └── imagens/      (fotos e capas em WebP, ilustrações em SVG)
```

## Como executar localmente

1. Baixe ou clone o repositório:
   ```bash
   git clone https://github.com/predobrito/Biblioteca-Digital-UniFECAF.git
   ```
2. Abra a pasta e dê dois cliques em `index.html`.
3. Mantenha as pastas `css/` e `assets/` ao lado do `index.html`.

As fontes são carregadas do Google Fonts e precisam de internet. Sem conexão, o navegador usa fontes alternativas (Arial / sans-serif).

## Observações

- Os livros exibidos são **demonstrativos**: capas e títulos foram tirados da biblioteca da UniFECAF só para ilustrar o projeto.
- A marca no topo é um símbolo criado em CSS para este trabalho. Não é o logotipo oficial.
- Informações oficiais da biblioteca: https://www.unifecaf.com.br/biblioteca

## Autor

**Pedro Augusto Brito Castilho Pereira**
Ciência da Computação – 5º semestre (noite) – Centro Universitário UniFECAF
Taboão da Serra, novembro de 2026

## Fontes de consulta

- [W3Schools – HTML e CSS](https://www.w3schools.com/)
- [Material Design](https://m2.material.io/)
- [MDN Web Docs – Elementos HTML](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element)
- [Bootstrap](https://getbootstrap.com/) (apenas como referência de grid e responsividade, sem uso no projeto)
- [WCAG 2.1 – W3C](https://www.w3.org/TR/WCAG21/)
