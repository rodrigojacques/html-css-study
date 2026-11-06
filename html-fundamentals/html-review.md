# HTML

---

<details>
<summary>Boas práticas</summary>

#### Semântica e acessibilidade

- Preferir elementos semânticos em vez de `div` e `span` quando houver um elemento mais adequado.
- Fornecer textos `alt` descritivos para imagens informativas e `alt=""` para imagens puramente decorativas.
- Associar cada `label` ao seu campo utilizando `for` e `id`.
- Manter uma hierarquia lógica de títulos, sem escolher níveis apenas pela aparência visual.
- Utilizar atributos ARIA somente quando os recursos nativos do HTML não forem suficientes.
- Escrever textos descritivos para links, evitando expressões genéricas como "clique aqui".

#### SEO e metadados

- Definir um `title` único e descritivo para cada página.
- Fornecer uma `meta name="description"` relevante para o conteúdo.
- Utilizar títulos e elementos semânticos que representem corretamente a estrutura da página.

#### Desempenho

- Otimizar imagens antes de publicá-las, utilizando formatos modernos como WebP ou AVIF quando apropriado.
- Utilizar `loading="lazy"` em imagens que não precisam ser carregadas imediatamente.
- Utilizar `defer` ou `async` em scripts externos quando apropriado.

#### Validação

- Validar o HTML com o [W3C Markup Validation Service](https://validator.w3.org/).
- Utilizar ferramentas como Lighthouse e WAVE para identificar problemas de acessibilidade e qualidade.

</details>

<details>
<summary>Conceitos de HTML</summary>

#### Tags, elementos e atributos

- **Tag:** marcação utilizada para identificar o início ou o fim de um elemento.
- **Elemento:** estrutura completa, geralmente formada por tag de abertura, atributos, conteúdo e tag de fechamento.
- **Atributo:** informação adicional configurada na tag de abertura.
- **Elemento vazio (Void):** não possui conteúdo interno nem tag de fechamento, como `<img>`, `<br>` e `<input>`.

#### Elementos de bloco e em linha

- **Bloco (Block):** comportamento de exibição que geralmente inicia uma nova linha e ocupa toda a largura disponível.
- **Em linha (Inline):** comportamento de exibição que ocupa apenas o espaço necessário ao conteúdo, sem iniciar uma nova linha.

Esses comportamentos podem ser alterados com CSS usando a propriedade `display`.

</details>

<details>
<summary>Atributos HTML</summary>
<br>

Atributos fornecem informações adicionais ou configuram o comportamento dos elementos HTML.

#### Atributos globais

Podem ser utilizados na maioria dos elementos HTML.

| Atributo | Função                                                       |
| -------- | ------------------------------------------------------------ |
| `id`     | Identifica um elemento de forma única dentro do documento.   |
| `class`  | Agrupa elementos para aplicação de estilos ou identificação. |
| `title`  | Fornece informações adicionais sobre um elemento.            |
| `lang`   | Define o idioma do conteúdo.                                 |
| `hidden` | Indica que o elemento não deve ser exibido.                  |

#### Atributos de links

| Atributo | Função                                                        |
| -------- | ------------------------------------------------------------- |
| `href`   | Define o destino de um link.                                  |
| `target` | Define onde o destino será aberto.                            |
| `rel`    | Define a relação entre o documento atual e o destino do link. |

#### Atributos de mídia

| Atributo   | Função                                                               |
| ---------- | -------------------------------------------------------------------- |
| `src`      | Define o caminho do arquivo de mídia.                                |
| `alt`      | Fornece uma descrição textual para imagens.                          |
| `width`    | Define a largura.                                                    |
| `height`   | Define a altura.                                                     |
| `controls` | Exibe controles de reprodução de áudio ou vídeo.                     |
| `loading`  | Define quando uma imagem ou conteúdo incorporado deve ser carregado. |

#### Atributos de formulários

| Atributo      | Função                                                     |
| ------------- | ---------------------------------------------------------- |
| `type`        | Define o tipo de entrada ou comportamento do elemento.     |
| `name`        | Identifica o campo quando os dados são enviados.           |
| `value`       | Define o valor de um campo.                                |
| `placeholder` | Exibe uma dica dentro de um campo.                         |
| `required`    | Torna o preenchimento obrigatório.                         |
| `disabled`    | Desabilita um elemento.                                    |
| `checked`     | Define um checkbox ou radio como selecionado inicialmente. |

</details>

<details>
<summary>Formulários</summary>
<br>

| Elemento     | Função                                 |
| ------------ | -------------------------------------- |
| `<form>`     | Agrupa campos e define um formulário.  |
| `<input>`    | Cria um campo de entrada de dados.     |
| `<label>`    | Identifica um campo do formulário.     |
| `<textarea>` | Cria um campo para textos maiores.     |
| `<select>`   | Cria uma lista de opções.              |
| `<option>`   | Define uma opção dentro de `<select>`. |
| `<button>`   | Cria um botão.                         |

</details>

<details>
<summary>HTML semântico</summary>
<br>

HTML semântico utiliza elementos que descrevem o significado e a função de cada parte da página, em vez de utilizar apenas contêineres genéricos como `<div>`.

| Elemento       | Função                                                                |
| -------------- | --------------------------------------------------------------------- |
| `<header>`     | Cabeçalho de uma página ou seção.                                     |
| `<nav>`        | Área que reúne links de navegação.                                    |
| `<main>`       | Representa o conteúdo principal da página.                            |
| `<article>`    | Representa um conteúdo independente, como uma notícia ou publicação.  |
| `<section>`    | Agrupa conteúdos relacionados a um mesmo assunto.                     |
| `<aside>`      | Representa conteúdo complementar, como uma barra lateral.             |
| `<footer>`     | Rodapé de uma página ou seção.                                        |
| `<figure>`     | Agrupa conteúdo independente, como imagens, ilustrações ou diagramas. |
| `<figcaption>` | Define uma legenda para o conteúdo de um `<figure>`.                  |

**Como diferenciar os principais elementos?**

- `<main>`: conteúdo principal da página.
- `<article>`: conteúdo independente que faz sentido por si só.
- `<section>`: divisão temática que agrupa conteúdos relacionados.
- `<div>`: contêiner genérico, sem significado semântico próprio.

**Por que utilizar HTML semântico?**

- Melhora a acessibilidade.
- Ajuda mecanismos de busca a compreender a estrutura da página.
- Torna o código mais organizado e fácil de manter.

</details>

<details>
<summary>Mídia e links</summary>
<br>

| Elemento   | Função                                                                               |
| ---------- | ------------------------------------------------------------------------------------ |
| `<a>`      | Cria links para outras páginas ou locais.                                            |
| `<img>`    | Exibe imagens.                                                                       |
| `<video>`  | Incorpora vídeos.                                                                    |
| `<audio>`  | Incorpora arquivos de áudio.                                                         |
| `<source>` | Define fontes alternativas de mídia para elementos como `<video>` e `<audio>`.       |
| `<iframe>` | Incorpora outra página ou conteúdo externo dentro do documento, como vídeos e mapas. |

</details>

<details>
<summary>Elementos de texto</summary>
<br>

| Elemento          | Função                                                          |
| ----------------- | --------------------------------------------------------------- |
| `<h1>` até `<h6>` | Define títulos e subtítulos em diferentes níveis hierárquicos.  |
| `<p>`             | Representa um parágrafo.                                        |
| `<strong>`        | Indica que o conteúdo possui forte importância.                 |
| `<em>`            | Dá ênfase ao conteúdo.                                          |
| `<span>`          | Contêiner genérico em linha, sem significado semântico próprio. |
| `<br>`            | Insere uma quebra de linha.                                     |
| `<hr>`            | Representa uma separação temática entre conteúdos.              |

</details>

<details>
<summary>Listas</summary>
<br>

| Elemento | Função                             |
| -------- | ---------------------------------- |
| `<ul>`   | Cria uma lista não ordenada.       |
| `<ol>`   | Cria uma lista ordenada.           |
| `<li>`   | Representa cada item de uma lista. |

</details>

<details>
<summary>Estrutura do documento</summary>
<br>

| Elemento          | Função                                                                           |
| ----------------- | -------------------------------------------------------------------------------- |
| `<!DOCTYPE html>` | Informa ao navegador que o documento utiliza HTML5.                              |
| `<html>`          | Elemento raiz que envolve todo o documento.                                      |
| `<head>`          | Armazena metadados e configurações da página.                                    |
| `<body>`          | Contém o conteúdo exibido na página.                                             |
| `<title>`         | Define o título exibido na aba do navegador.                                     |
| `<meta>`          | Define metadados, como codificação de caracteres e configuração de visualização. |
| `<link>`          | Relaciona o documento a recursos externos, como folhas de estilo e favicon.      |
| `<script>`        | Insere ou referencia código JavaScript.                                          |

</details>

---

**Referência:** [MDN Web Docs — HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
