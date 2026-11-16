# Portfólio · Matheus Ávila

Link do portifólio: https://matheusavila-dev.github.io/Portifolio-Web-Matheus/

Portfólio web de desenvolvedor Full Stack, feito em HTML, CSS e JavaScript puro, em um único arquivo, sem dependências nem etapa de build. O site é bilíngue (Português do Brasil e Inglês), tem tema claro e escuro, e é responsivo.

## Funcionalidades

- **Header fixo** com logo, navegação (Início, Sobre, Habilidades, Projetos, Contato), botão de idioma (PT/EN) e botão de tema (claro/escuro). No celular, a navegação vira um menu.
- **Início, Sobre, Habilidades, Projetos e Contato** em uma página só, com destaque automático do item de menu da seção visível.
- **Página “Outros projetos”**, acessada por `#outros-projetos`, com o mesmo header e footer.
- **Formulário de contato** (nome, número, e-mail e mensagem) com dois envios: por e-mail (`mailto:`) e por WhatsApp (`wa.me`).
- **Animações sutis** de entrada e saída ao rolar a página, via `IntersectionObserver`. Não há animação que siga o mouse e, com `prefers-reduced-motion`, as animações são desativadas.
- **Tema e idioma persistidos** no `localStorage` (com `try/catch`, então o site funciona mesmo se o armazenamento estiver bloqueado).
- **Footer** com navegação, contatos e botão “Voltar ao topo”.

## Paleta

| Uso | Cor |
| --- | --- |
| Roxo principal | `#6b1fad` |
| Fundo claro / escuro | branco e preto, com variações sutis |
| Roxo de apoio no tema escuro | `#b27be6` (para manter a legibilidade) |

As cores são variáveis CSS definidas em `:root`, com versões para o tema claro e para o escuro.

## Arquitetura (MVC)

Todo o JavaScript fica no mesmo arquivo, separado em três camadas:

| Camada | Objeto | Responsabilidade |
| --- | --- | --- |
| **Model** | `Model` | Configurações (`cfg`), estado (idioma e tema), textos PT/EN, habilidades e projetos |
| **View** | `V` | Funções que geram o HTML de cada parte (header, home, outros projetos, footer, cartões) |
| **Controller** | `C` | Inicialização, rotas por hash, tema, idioma, observadores de scroll e eventos de clique |

## Estrutura de arquivo

```
index.html
README.md
assets/
```

## Detalhes técnicos

- HTML semântico (`header`, `nav`, `main`, `section`, `footer`, `article`, `form` com `label`).
- Responsivo, sem rolagem horizontal, com suporte a `safe-area` em celulares com notch.
- Acessibilidade: `aria-label` nos botões, `aria-expanded` no menu, `aria-current` na navegação e foco visível nos campos.
- Rotas por hash (`#sobre`, `#projetos`, `#outros-projetos` etc.), então não precisa de servidor.
- O botão de WhatsApp usa o número `5534988387442`, e o de e-mail usa `matheusdeaviladev@gmail.com`. Ambos estão em `Model.cfg`.

## Contato

- E-mail: matheusdeaviladev@gmail.com
- Telefone / WhatsApp: (34) 98838-7442
- Instagram: [@matheusavila.dev](https://instagram.com/matheusavila.dev)
- GitHub: [matheusavila-dev](https://github.com/matheusavila-dev)
- LinkedIn: Matheus Ávila

---

Feito por Matheus Borges Ávila, fundador da [nex7step](https://nex7step.up.railway.app).
