# Conexão em Casa

Site com instruções simples para resolver problemas comuns de conexão com a internet, que qualquer pessoa pode seguir em casa, sem conhecimento técnico.

**Acesse o site:** https://lucaskruppa.github.io/atividadeFinalIHC2B2P/

## Páginas

| Página | Função |
|---|---|
| `index.html` | Explica o objetivo do site e direciona o usuário ao problema dele |
| `lentidao.html` | Passo a passo para internet lenta |
| `desconexao.html` | Passo a passo para internet que caiu |

## Conceitos aplicados

### Usabilidade
- **Consistência:** o mesmo cabeçalho e menu em todas as páginas, para o usuário sempre saber onde encontrar a navegação.
- **Localização:** a página atual fica destacada no menu (negrito e linha inferior).
- **Caminho claro:** a página inicial oferece dois cards grandes e clicáveis, um para cada problema.
- **Área de toque:** os links do menu têm espaçamento vertical para facilitar o toque no celular.
- **Leitura confortável:** largura máxima do conteúdo e espaçamento entre linhas.

### Experiência do Usuário (UX)
- **Linguagem simples:** os cards descrevem o sintoma ("páginas demoram a carregar"), e não termos técnicos.
- **Passos numerados com saída:** cada passo termina dizendo o que fazer se resolveu ou não, para o usuário não perder tempo.
- **Sem becos sem saída:** toda página termina com um aviso para procurar o provedor quando nada resolver.
- **Feedback visual:** os cards e links reagem ao passar o mouse.
- **Modo escuro:** o usuário escolhe o tema que for mais confortável.
- **Triagem inicial:** ambas as páginas de instruções incluem um card com diagnóstico inicial para o usuário seguir.

### Acessibilidade
- Idioma declarado (`lang="pt-BR"`) para leitores de tela.
- Tags semânticas (`header`, `nav`, `main`, `section`, `footer`) e hierarquia de títulos (`h1`, `h2`).
- Passos em lista ordenada (`<ol>`), para o leitor de tela anunciar a posição do passo.
- Menu identificado com `aria-label` e página atual marcada com `aria-current="page"`.
- Botão de modo escuro com `<label>` ligado ao `<input>`, utilizável pelo espaço do teclado.
- Foco visível (`:focus-visible`) em links, cards e botão.
- Link "Pular para o conteúdo" para quem navega pelo teclado.
- Contraste de cores acima de 4,5:1 (padrão WCAG) nos dois temas.
- Medidas em `rem`, que acompanham o tamanho de fonte do usuário e funcionam com zoom de 200%.
- Destaque da página atual com mais do que cor (negrito e linha).

### Responsividade
- `<meta name="viewport">` em todas as páginas.
- Cards com Flexbox (`flex-wrap` e `flex: 1 1 18rem`), que ficam lado a lado em telas largas e empilham sozinhos nas estreitas.
- Menu com `flex-wrap`, para os links quebrarem de linha em vez de estourar a tela.
- Testado em larguras de celular e com zoom de 200%.

## Escolhas de design

- **Paleta com variáveis CSS:** as cores ficam em `:root`, e o modo escuro só troca os valores das variáveis. O resto do CSS não precisa ser repetido.
- **Modo escuro sem JavaScript:** um checkbox escondido, um `<label>` como botão e o seletor `:has(:checked)`. Foi escolhido para manter o projeto só com HTML e CSS.
  - **Limitação:** sem JavaScript, a escolha não é guardada ao mudar de página.
  - O seletor `:has()` não funciona em navegadores muito antigos.
- **Azul marinho:** cor associada a tecnologia e confiança, com contraste verificado.
- **Estrutura de 3 páginas:** uma de contexto e duas de instruções, para cada página ter um único propósito.

## Relação com os conteúdos estudados

### Heurísticas de Nielsen
| Heurística | Como aparece no site |
|---|---|
| Visibilidade do status do sistema | A página atual fica destacada no menu, e os passos numerados mostram em que etapa o usuário está. |
| Correspondência com o mundo real | Os cards descrevem o sintoma ("páginas demoram a carregar") em linguagem do dia a dia. |
| Controle e liberdade do usuário | O menu fica sempre visível, cada passo diz que o usuário pode parar se resolveu, e o modo escuro pode ser desligado a qualquer momento. |
| Consistência e padrões | Mesmo cabeçalho, menu, rodapé e cores (variáveis CSS) em todas as páginas; as páginas de passos seguem o mesmo molde. |
| Prevenção de erros | Avisos preventivos nos passos, como não forçar o cabo de fibra. |
| Reconhecimento em vez de memorização | O usuário escolhe o problema reconhecendo o sintoma nos cards, sem precisar lembrar termos técnicos. |
| Flexibilidade e eficiência de uso | Link "Pular para o conteúdo", navegação completa por teclado e acesso direto ao problema pela página inicial. |
| Design estético e minimalista | Poucos elementos por página e um caminho principal claro. |
| Ajudar a recuperar de erros | Cada passo diz o que fazer se o problema continuar, e o aviso final indica o provedor. |
| Ajuda e documentação | O site inteiro é um guia de instruções. |

### User Experience e Design Centrado no Usuário
- **Público:** pessoas sem conhecimento técnico, com um problema de internet em casa.
- **Tarefa do usuário:** identificar o problema e seguir os passos para resolvê-lo.
- O conteúdo e a estrutura foram organizados em torno dessa tarefa: linguagem simples, tempo estimado e passos com saída.

### Cores, Tipografia e Acessibilidade
- **Cores:** azul marinho com fundo claro e versão escura, definidas por variáveis CSS. O contraste entre texto e fundo foi conferido e fica acima de 4,5:1 nos dois temas.
- **Tipografia:** fonte sem serifa (Arial), espaçamento entre linhas de 1,6, hierarquia de títulos (`h1` maior que `h2`) e medidas em `rem`.
- **Acessibilidade:** ver os itens listados em "Acessibilidade" acima.

### Engenharia Semiótica
- A interface é a forma de o designer "conversar" com o usuário: o título, a frase de apresentação e os dois cards da página inicial dizem quem o site atende e como usá-lo.

### Prototipação
- Antes de programar, as telas foram planejadas em esboços de baixa fidelidade (a disposição dos blocos de cada página).

## Tarefas realizadas

| Integrante | Tarefas |
|---|---|
| Lucas Kruppa | Projeto individual: planejamento, HTML das 3 páginas, CSS (tema, layout, modo escuro, responsividade, acessibilidade), publicação no GitHub Pages e este README |

## Estrutura do projeto

```text
index.html
lentidao.html
desconexao.html
style.css
README.md
```