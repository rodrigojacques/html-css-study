# HTML

---

<details>
<summary><strong>Boas práticas</strong></summary>

#### Semântica e acessibilidade

- Preferir elementos semânticos em vez de `div` e `span` quando houver um elemento mais adequado.
- Definir o idioma principal do documento utilizando o atributo `lang` no elemento `<html>`.
- Fornecer textos `alt` descritivos para imagens informativas e `alt=""` para imagens puramente decorativas.
- Associar cada `label` ao seu campo utilizando `for` e `id`.
- Manter uma hierarquia lógica de títulos.
- Garantir que elementos interativos possam ser utilizados por teclado e tenham indicadores visíveis de foco.
- Garantir contraste adequado entre texto e fundo.
- Utilizar atributos ARIA somente quando os recursos nativos do HTML não forem suficientes.
- Escrever textos descritivos para links, evitando expressões genéricas.

#### SEO e metadados

- Utilizar HTML semântico para facilitar a compreensão da estrutura e do conteúdo da página.
- Definir um título único e descritivo e fornecer uma meta description relevante para cada página.
- Produzir conteúdo de qualidade, organizado e relevante para o público.
- Garantir uma boa experiência em dispositivos móveis.

#### Desempenho

- Otimizar imagens antes de publicá-las, utilizando formatos modernos como WebP ou AVIF quando apropriado.
- Especificar `width` e `height` nas imagens para ajudar a evitar mudanças inesperadas no layout durante o carregamento.
- Utilizar `loading="lazy"` em imagens que não precisam ser carregadas imediatamente, evitando aplicá-lo às imagens importantes inicialmente visíveis.
- Utilizar `defer` ou `async` em scripts externos quando apropriado.

#### Estrutura e organização

- Evitar IDs duplicados no mesmo documento.
- Manter o HTML organizado, indentado e com elementos corretamente aninhados.

#### Validação

- Validar o HTML com o [W3C Markup Validation Service](https://validator.w3.org/).
- Utilizar ferramentas como Lighthouse e WAVE para identificar problemas de acessibilidade, desempenho e qualidade.

</details>

<details>
<summary><strong>Conceitos de HTML</strong></summary>

#### Tags, elementos e atributos

- **Tag:** marcação utilizada para identificar o início ou o fim de um elemento.
- **Elemento:** estrutura completa, geralmente formada por tag de abertura, atributos, conteúdo e tag de fechamento.
- **Atributo:** informação adicional configurada na tag de abertura.
- **Elemento vazio (Void):** não possui conteúdo interno nem tag de fechamento, como `<img>`, `<br>` e `<input>`.

#### Elementos de bloco e em linha

- **Bloco (Block):** comportamento de exibição que geralmente inicia uma nova linha e ocupa toda a largura disponível.
- **Em linha (Inline):** comportamento de exibição que ocupa apenas o espaço necessário ao conteúdo, sem iniciar uma nova linha.

Esses comportamentos podem ser alterados com CSS usando a propriedade `display`.

#### Contêineres genéricos

| Elemento | Função |
| -------- | ----- |
| `<div>` | Contêiner genérico de bloco, sem significado semântico próprio. |
| `<span>` | Contêiner genérico em linha, sem significado semântico próprio. |

</details>

<details>
<summary><strong>Atributos HTML</strong></summary>
<br>

Atributos fornecem informações adicionais ou configuram o comportamento dos elementos HTML.

#### Atributos globais

Podem ser utilizados na maioria dos elementos HTML.

| Atributo | Função |
| -------- | ----- |
| `id` | Identifica um elemento de forma única dentro do documento. |
| `class` | Agrupa elementos para aplicação de estilos ou identificação. |
| `title` | Fornece informações adicionais sobre um elemento. |
| `lang` | Define o idioma do conteúdo. |
| `hidden` | Indica que o elemento não deve ser apresentado. |

#### Atributos de links

| Atributo | Função |
| -------- | ----- |
| `href` | Define o destino de um link. |
| `target` | Define onde o destino será aberto. |
| `rel` | Define a relação entre o documento atual e o destino do link. |

Ao utilizar `target="_blank"`, é uma boa prática incluir `rel="noopener noreferrer"`.

#### Atributos de imagens e mídia

| Atributo | Função |
| -------- | ----- |
| `src` | Define o caminho do arquivo de mídia. |
| `alt` | Fornece uma descrição textual para imagens. |
| `width` | Define a largura. |
| `height` | Define a altura. |
| `controls` | Exibe controles de reprodução de áudio ou vídeo. |
| `loading` | Define quando uma imagem ou conteúdo incorporado deve ser carregado, utilizando valores como `lazy` ou `eager`. |

#### Atributos de formulários

| Atributo | Função |
| -------- | ----- |
| `type` | Define o tipo de entrada ou comportamento do elemento. |
| `name` | Identifica o campo quando os dados são enviados. |
| `value` | Define o valor de um campo. |
| `placeholder` | Exibe uma dica dentro de um campo. |
| `required` | Torna o preenchimento obrigatório. |
| `disabled` | Desabilita um elemento; seu valor não é enviado com o formulário. |
| `readonly` | Impede a edição do campo, mas permite que seu valor seja enviado. |
| `checked` | Define um checkbox ou radio como selecionado inicialmente. |
| `min` / `max` | Definem os valores mínimo e máximo permitidos. |
| `minlength` / `maxlength` | Definem os comprimentos mínimo e máximo do texto. |
| `pattern` | Define um padrão que o valor precisa seguir. |

**Observação:** campos precisam de um atributo `name` para que seus valores sejam incluídos no envio do formulário. O `placeholder` não substitui o uso de um `label`.

</details>

<details>
<summary><strong>Formulários</strong></summary>
<br>

| Elemento | Função |
| -------- | ----- |
| `<form>` | Agrupa campos e define um formulário. |
| `<input>` | Cria um campo de entrada de dados. |
| `<label>` | Identifica um campo do formulário. |
| `<textarea>` | Cria um campo para textos maiores. |
| `<select>` | Cria uma lista de opções. |
| `<option>` | Define uma opção dentro de `<select>`. |
| `<button>` | Cria um botão. |
| `<fieldset>` | Agrupa campos relacionados dentro de um formulário. |
| `<legend>` | Define uma legenda ou título para um `<fieldset>`. |

#### Atributos de envio do formulário

| Atributo | Função |
| -------- | ----- |
| `action` | Define o endereço para o qual os dados do formulário serão enviados. |
| `method` | Define o método HTTP utilizado no envio (`GET` ou `POST`). |
| `enctype` | Define como os dados serão codificados durante o envio. |
| `autocomplete` | Controla o preenchimento automático dos campos. |
| `novalidate` | Desativa a validação nativa do formulário durante o envio. |

#### Métodos HTTP

- **GET:** envia os dados pela URL, geralmente utilizado para consultas e buscas. Os parâmetros podem ser compartilhados ou favoritados.
- **POST:** envia os dados no corpo da requisição HTTP, geralmente utilizado para enviar informações ao servidor.

**Importante:** GET e POST não garantem, por si só, a segurança dos dados. O HTTPS é necessário para proteger a comunicação entre navegador e servidor.

**Exemplo:**

```html
<form action="/register" method="POST">
  <label for="email">Email:</label>
  <input type="email" id="email" name="email" required />

  <button type="submit">Register</button>
</form>
```

</details>

<details>
<summary><strong>HTML semântico</strong></summary>
<br>

HTML semântico utiliza elementos que descrevem o significado e a função de cada parte da página, em vez de utilizar apenas contêineres genéricos como `<div>`.

| Elemento | Função |
| -------- | ----- |
| `<header>` | Cabeçalho de uma página ou seção. |
| `<nav>` | Área que reúne links de navegação. |
| `<main>` | Representa o conteúdo principal da página. |
| `<article>` | Representa um conteúdo independente, como uma notícia ou publicação. |
| `<section>` | Agrupa conteúdos relacionados a um mesmo assunto. |
| `<aside>` | Representa conteúdo complementar, como uma barra lateral. |
| `<footer>` | Rodapé de uma página ou seção. |
| `<figure>` | Agrupa conteúdo independente, como imagens, ilustrações ou diagramas. |
| `<figcaption>` | Define uma legenda para o conteúdo de um `<figure>`. |
| `<time>` | Representa uma data ou horário, podendo fornecer uma versão legível por máquinas através do atributo `datetime`. |

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
<summary><strong>Mídia e links</strong></summary>
<br>

| Elemento | Função |
| -------- | ----- |
| `<a>` | Cria links para outras páginas ou locais. |
| `<img>` | Exibe imagens. |
| `<picture>` | Permite definir diferentes fontes de imagem para situações como responsividade e formatos alternativos. |
| `<video>` | Incorpora vídeos. |
| `<audio>` | Incorpora arquivos de áudio. |
| `<source>` | Define fontes alternativas de mídia para elementos como `<picture>`, `<video>` e `<audio>`. |
| `<iframe>` | Incorpora outra página ou conteúdo externo dentro do documento, como vídeos e mapas. |

</details>

<details>
<summary><strong>Elementos de texto</strong></summary>
<br>

| Elemento | Função |
| -------- | ----- |
| `<h1>` até `<h6>` | Define títulos e subtítulos em diferentes níveis hierárquicos. |
| `<p>` | Representa um parágrafo. |
| `<strong>` | Indica que o conteúdo possui forte importância. |
| `<em>` | Dá ênfase ao conteúdo. |
| `<br>` | Insere uma quebra de linha. |
| `<hr>` | Representa uma separação temática entre conteúdos. |
| `<code>` | Representa um trecho de código de computador. |
| `<pre>` | Preserva espaços e quebras de linha do conteúdo, sendo frequentemente utilizado para exibir blocos de código. |
| `<blockquote>` | Representa uma citação em bloco. |
| `<q>` | Representa uma citação curta em linha. |
| `<cite>` | Representa o título de uma obra criativa citada. |
| `<abbr>` | Representa uma abreviação ou sigla, podendo utilizar o atributo `title` para fornecer sua descrição completa. |

</details>

<details>
<summary><strong>Listas</strong></summary>
<br>

| Elemento | Função |
| -------- | ----- |
| `<ul>` | Cria uma lista não ordenada. |
| `<ol>` | Cria uma lista ordenada. |
| `<li>` | Representa cada item de uma lista. |
| `<dl>` | Cria uma lista de termos e suas descrições. |
| `<dt>` | Define o termo ou nome que será descrito. |
| `<dd>` | Fornece a descrição ou definição do termo. |

**Exemplo:**

```html
<dl>
  <dt>HTML</dt>
  <dd>Linguagem de marcação utilizada para estruturar páginas web.</dd>

  <dt>CSS</dt>
  <dd>Linguagem utilizada para estilizar páginas web.</dd>
</dl>
```

</details>

<details>
<summary><strong>Tabelas</strong></summary>
<br>

| Elemento | Função |
| -------- | ----- |
| `<table>` | Cria uma tabela para organizar dados em linhas e colunas. |
| `<caption>` | Define o título ou uma legenda para a tabela. |
| `<thead>` | Agrupa as linhas que representam o cabeçalho da tabela. |
| `<tbody>` | Agrupa as linhas que representam o conteúdo principal da tabela. |
| `<tfoot>` | Agrupa as linhas que representam o rodapé da tabela. |
| `<tr>` | Define uma linha da tabela. |
| `<th>` | Define uma célula de cabeçalho. |
| `<td>` | Define uma célula de dados. |

</details>

<details>
<summary><strong>Elementos interativos</strong></summary>
<br>

| Elemento | Função |
| -------- | ----- |
| `<details>` | Cria um componente que pode ser expandido ou recolhido pelo usuário. |
| `<summary>` | Define o título ou rótulo clicável de um elemento `<details>`. |

**Exemplo:**

```html
<details>
  <summary>More information</summary>
  <p>Additional content goes here.</p>
</details>
```

</details>

<details>
<summary><strong>Estrutura do documento</strong></summary>
<br>

| Elemento | Função |
| -------- | ----- |
| `<!DOCTYPE html>` | Declara que o documento utiliza o padrão moderno de HTML e ajuda a evitar o modo de compatibilidade (quirks mode). |
| `<html>` | Elemento raiz que envolve todo o documento. |
| `<head>` | Armazena metadados e configurações da página. |
| `<body>` | Contém o conteúdo exibido na página. |
| `<title>` | Define o título exibido na aba do navegador. |
| `<meta>` | Define metadados, como codificação de caracteres e configuração de visualização. |
| `<link>` | Relaciona o documento a recursos externos, como folhas de estilo e favicon. |
| `<script>` | Insere ou referencia código JavaScript. |

</details>

<details>
<summary><strong>Metadados e SEO</strong></summary>
<br>

Metadados são informações sobre a página, geralmente declaradas dentro de `<head>`. Eles ajudam navegadores, mecanismos de busca e plataformas externas a interpretar e apresentar o conteúdo.

#### Metadados básicos

| Recurso | Função |
| ------- | ----- |
| `charset` | Define a codificação de caracteres. |
| `viewport` | Configura a visualização em dispositivos móveis. |
| `author` | Identifica o autor do conteúdo da página. |
| `description` | Fornece uma descrição resumida da página, que pode aparecer nos resultados de busca. |

**Exemplo:**

```html
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<meta name="author" content="Author Name" />
<meta name="description" content="A description of the page." />
```

#### SEO e compartilhamento

| Recurso | Função |
| ------- | ----- |
| `rel="canonical"` | Indica a URL preferencial quando existem páginas duplicadas ou semelhantes. |
| `name="robots"` | Define instruções para mecanismos de busca, como permitir ou impedir a indexação. |
| Open Graph | Controla como o conteúdo aparece quando compartilhado em redes sociais e aplicativos de mensagens. |

**Exemplo de canonical e robots:**

```html
<link rel="canonical" href="https://example.com/page" />
<meta name="robots" content="noindex, follow" />
```

**Observação:** `noindex` solicita que mecanismos de busca não incluam a página nos resultados de busca. O atributo `robots` não é um mecanismo de segurança ou controle de acesso.

**Principais propriedades Open Graph:**

| Propriedade | Função |
| ----------- | ----- |
| `og:title` | Título do compartilhamento. |
| `og:description` | Descrição do conteúdo. |
| `og:image` | Imagem de apresentação. |
| `og:image:alt` | Descrição da imagem. |
| `og:url` | URL da página. |
| `og:type` | Tipo de conteúdo, como `website` ou `article`. |
| `og:site_name` | Nome do site. |

**Exemplo:**

```html
<meta property="og:title" content="Page Title" />
<meta property="og:description" content="A description of the page." />
<meta property="og:image" content="https://example.com/image.jpg" />
<meta property="og:image:alt" content="Description of the image" />
<meta property="og:url" content="https://example.com/page" />
<meta property="og:type" content="website" />
<meta property="og:site_name" content="Example" />
```

**Recomendação:** uma dimensão comum para imagens Open Graph é `1200 × 630 px`, com proporção aproximada de `1.91:1`.

#### Outros recursos

| Recurso | Função |
| ------- | ----- |
| Twitter Cards | Personaliza a apresentação de links no X. Pode aproveitar propriedades Open Graph. |
| `theme-color` | Sugere a cor da interface do navegador em plataformas compatíveis. |
| Web App Manifest | Arquivo de configuração utilizado em Progressive Web Apps (PWA). |
| `hreflang` | Indica versões linguísticas ou regionais de uma página. |
| JSON-LD | Formato utilizado para fornecer dados estruturados aos mecanismos de busca. |

**Exemplos:**

```html
<meta name="twitter:card" content="summary_large_image" />

<meta name="theme-color" content="#ffffff" />

<link rel="manifest" href="/manifest.webmanifest" />
```

</details>

---

**Referência:** [MDN Web Docs — HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
