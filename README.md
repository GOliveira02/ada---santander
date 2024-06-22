# Ada - Santander Coders
Este repositório foi criado com a função de armazenar os processos do curso Santander Coders, pela empresa ADA. Este arquivo Markdown resumirá o caderno de anotações e resultados dos processos.
## Curso online
### Caderno de anotações
#### Git e Versionamento ----------------------------------------------------------------
> Versionamento e seus estados

O versionamento é o registro das alterações de um programa, onde pode-se fazer uso de versões anteriores para recuperar funcionalidades, ou recuperar versões que não continham um determinado erro, dentre outras funções. Ex: v. 1.1, v. 2.3.2, v. 3.0

O Git pe um sistema de versionamento de código que salva referencias de dados em momentos de um programa. A maioria dos Gits são feitos na máquina para que se tennha mais facilidade na hora de localizar e/ou transferir arquivos.

O Git na máquina é uma opção de Git local, mas existem opções de Gits externos, coomo é o caso do GitHub, um sistema Git online.

Um arquivo pode ter 4 modos. Eles são:

 Untracked| Unmodified | Modified | Staged 
|---------|------------|----------|-------|
|Quando o arquivo ou alteração não é rastreado| Quando o arquivo está salvo | Quando o arquivo é modificado| Quando o qrquivo está pronto para receber Commit

A ordem de modificações de um arquivo, sob os 4 modos é:
Untracked| Unmodified | Modified | Staged 
|---------|------------|----------|-------|
|Primeiro se cria o arquivo e, quando ele não é salvo, ele está Entracked, e quando se salva o arquivo, ele está Unmodified|Unmodified é o estado onde o arquivo está salvo, sem alteração alguma desde seu ultimo salvamento| Então, quando se altera algo, o arquivo está Modified, já que existem alterações não salvas, e para iniciar o processo de salvamento, usa-se "git add"| Por fim, temos o Staged, onde se tem o arquivo quase salvo, é uma forma de dizer ao computador que você está preparado para das o Commit no arquivo

> Branch

Bratchs são ramificações de um código, onde, se é possivel duas ou mais pessoas altearem um mesmo código de forma que possam uní-los depois. Geralmente, a Branch principal é a "master".

Ex: Ao criar ma rede-social, o programador 1 está configurando o botão de login, enquanto o programador 2 está configurando o botão de cadastro. Quando ambos terminatem, poderão unir suas alterações (branch) para um único arquivo.

Para criar uma nova Brantch, usa-se o código "git bratch *nome da branch *", mas para começar a alterar sob esta branch, é preciso usar "git checkout *nome da branch *".

Ao se fazer alterações nas Branch's,  são criadas ramificações que podem não ser lidas de uma branch para a outra. Mas para mesclar as brunchs usa o comando "git merge *nome da branch *".

##### Lista de comandos git:
> git config --global user.name "nome do usuário" | Configura o nome do usuário daquela máquina

> git config --global user.email *email do usuário *| Configura o email do usuário daquela máquina

> git init | Inicia o git na pasta usada

> git add * nome do arquivo * | Passa o arquivo em questão de Modified para Staged 

> git commit -m "nome da atualização" | Faz o commit do arquivo, e passa ele de Staged para Unmodified

> git commit -am "nome da atualização" | Faz o commit de todos os arquivos que estão em estado de Modified sem precisar usar 'git add'

> git status |  Mostra o status do arquivo

> git diff | Mostra as alterações feitas no arquivo, quando está no status Modified

> git diff --staged | Mostra as alterações feitas no arquivo, quando está no status Staged

> git log | Mostra uma lista dos Commits junto do autor e o email do mesmo junto da mensagem do commit

> git restore *nome do arquivo *| É usado para restaurar o arquivo para o ultimo estado antes da alteração, mas caso o arquivo esteja em Stagad, é preciso acrescentar "--staged" como apredentado no comando abaixo

> git restore --staged *nome do arquivo *| Passa o arquivo de Staged para Modified, caso tenha usado o comando "git add"

> git pull | Quando há mais de um autor, e é feito uma alteração no repositório, este comando trará todas as alterações para o código a ser alterado, alterando-o

> git fetch | Quando há mais de um autor, e é feito uma alteração no repositório, este comando trará todas as alterações para o código a ser alterado, sem alterá-lo, então dá para usar o comando 'git diff origin/*nome da branch *' para mostras as alterações no repositório sem alterar seu código.

> git bratch *nome da branch * | Cria uma nova Branch

> git checkout *nome da branch * | Leva o autor, a partir do código, a alterar o arquivo nesta branch

> git log --online --decorate | Mostra uma lista de Commits, mas mostra o status de qual branch o autor está alterando no momento

> git merge *nome da branch * | Mescla a branch ao qual se coloca o nome à branch atual (talvez a master?)

#### HTML ----------------------------------------------------------------
HTML é uma linguagem de **marcação** utilizada na construção de páginas na Web, usada para criar a estrutura da página Web. E refere-se à forma,, hierarquia, ordem e/ou semantica.

A estrutura de um arquivo HTML conta com duas tags de extrema importancia:

| Head | Body|
|-----------------------------------------------|------------------------------------------|
| A tag `<head>` contém metadados sobre o documento. | A tag `<body>` contém o conteúdo principal do documento. |
| Inclui elementos como `<title>`, `<meta>`, `<link>`, `<style>`, e `<script>` (scripts que devem ser carregados no início). | Inclui elementos como texto, imagens, links, tabelas, formulários, e outros elementos interativos. |
| O conteúdo dentro da tag `<head>` não é exibido diretamente ao usuário. | O conteúdo dentro da tag `<body>` é exibido diretamente ao usuário no navegador. |
| Usado para definir o título do documento que aparece na aba do navegador. | Usado para estruturar e apresentar o conteúdo visual e interativo da página web. |
| Pode incluir folhas de estilo CSS para definir o design da página. | Pode incluir scripts e interações que serão executadas quando o conteúdo for exibido. |
| Exemplos: `<title>`, `<meta>`, `<link>`, `<style>`, `<script>` | Exemplos: `<h1>`, `<p>`, `<img>`, `<a>`, `<div>`, `<span>`, `<form>` |


Os elementos do HTML, geralmente, contem três componentes: a tag de abertura, o conteudo e a tag de fechamento, como por exemplo: 

- **Tags (marcação)**: Usadas para descrever (renderizar) o elemento adicionado, e delimitadas por "<" e ">". como: < button>, < p>, dentre outros.

A tag **Button** é estruturada com sintaxes de abertura e fechamento, a exemplo:
 
`<button> Esta é a tag de botão </button>`

<button> Esta é a tag de botão </button>

A tag **Parágrafo**:

`<p> "Esta é a tag de parágrafo" </p>`
<p> "Esta é a tag de parágrafo" </p>

É possivel, no HTML, aninhar tags, como, por exemplo, transformar uma imagem em um botão, ou acrescentar uma caixa de seleção em um parágrafo. Alem da possibilidade de dar caracteristicas às tags, como largura, comprimento, cor, opacidade, dentre outras.

Dentro de um arquivo HTML, existem predefinições básicas:
| Tag | Descrição|
|-----|----------|
| `<html>` | É a tag raiz que encapsula todo o conteúdo de um documento HTML.|
| `<head>` | Contém metadados e informações sobre o documento, como título e links para CSS.|
| `<title>`| Define o título da página que aparece na aba do navegador.|
| `<body>` | Contém o conteúdo principal do documento que será exibido no navegador.|
| `<h1>`   | Representa o título de nível 1, geralmente usado como o título principal da página. |
| `<p>`    | Define um parágrafo de texto.|
| `<div>`  | Define uma divisão ou seção no 

> Para fins de estudos, é possivel checar repositórios públicos, uma boa opção é o "MDN HTML".

- Quando dentro de um arquivo HTML, não adianta apertar enter duas vezes pasa quebrar a linha, por isso, pode-se usar a tag `<br>` para quebrar a linha. Se duas tags `<br>` forem colocadas na mesma linha, isso contará como dois espaços de linha, como:

~~~html
<p>Paralelepipedo <br><br> azul<p>
~~~
> <p>Paralelepipedo <br><br> azul<p>

- Tambem existe a linha horizontal para separar sessões, ela é demarcada pela tag `<hr>`, que fica

~~~HTML
<h3>O paralelepipedo azul</h3> <hr> <h4>O paralelepipedo azul não é rosa</h4>
~~~

><h3>O paralelepipedo azul</h3> <hr> <h4>O paralelepipedo azul não é rosa</h4>

~~~html
<!-- É com este comando que se coloca comentários no arquivo HTML -->, usando uma exclamação entre maior e menor que: <!-- -->
~~~

A tag `<a>` em HTML é utilizada para criar links, permitindo a navegação entre páginas web, documentos, ou mesmo diferentes partes de uma mesma página. A forma básica de usar a tag `<a>` é incluir um atributo `href` que especifica o destino do link. Aqui está um exemplo simples:

```html
<a href="https://www.example.com">Visite o Example</a>
```

### Atributos Comuns da Tag `<a>`

1. **href**
   O atributo `href` (hypertext reference) especifica o URL do destino do link. Pode ser um link absoluto (começando com `http://` ou `https://`) ou um link relativo.

   ```html
   <a href="https://www.example.com">Visite o Example</a>
   <a href="/pasta/pagina.html">Página Interna</a>
   ```

2. **target**
   O atributo `target` define onde o link será aberto. Os valores mais comuns para este atributo são:

   - `_self`: Abre o link na mesma janela ou aba (padrão).
   - `_blank`: Abre o link em uma nova janela ou aba.
   - `_parent`: Abre o link no frame pai (usado em contextos de frames).
   - `_top`: Abre o link no corpo inteiro da janela, removendo todos os frames.

   ```html
   <a href="https://www.example.com" target="_self">Link na Mesma Aba</a>
   <a href="https://www.example.com" target="_blank">Link em Nova Aba</a>
   ```

3. **title**
   O atributo `title` fornece um texto adicional sobre o link, que aparece quando o usuário passa o cursor sobre o link.

   ```html
   <a href="https://www.example.com" title="Visite Example">Link com Título</a>
   ```

4. **rel**
   O atributo `rel` especifica a relação entre o documento atual e o documento vinculado. Alguns valores comuns são:

   - `noopener`: Usado com `target="_blank"` para impedir que a página recém-aberta possa acessar a página original via `window.opener`.
   - `nofollow`: Informa aos motores de busca para não seguirem o link.
   - `noreferrer`: Não envia informações de referência ao destino do link.

   ```html
   <a href="https://www.example.com" target="_blank" rel="noopener">Link Seguro</a>
   <a href="https://www.example.com" rel="nofollow">Link Sem Seguimento</a>
   ```

### Exemplos Completos

#### Link Básico

```html
<a href="https://www.example.com">Visite o Example</a>
```

#### Link Abrindo em Nova Aba

```html
<a href="https://www.example.com" target="_blank">Visite o Example em Nova Aba</a>
```

#### Link Com Título

```html
<a href="https://www.example.com" title="Visite Example para mais informações">Mais Informações</a>
```

#### Link Seguro com `rel`

```html
<a href="https://www.example.com" target="_blank" rel="noopener noreferrer">Link Seguro</a>
```

### Comentários em HTML

Assim como mencionado anteriormente, os comentários em HTML são feitos usando `<!-- comentário -->`. Eles são úteis para incluir notas ou explicações dentro do código sem que sejam exibidas na página.

```html
<!-- Este é um comentário em HTML -->
<a href="https://www.example.com" target="_blank">Visite o Example</a>
```

Usar a tag `<a>` de forma eficaz permite criar links funcionais e acessíveis, aprimorando a navegação e a usabilidade do seu site.

Ao adicionar uma imagem, é preciso levar em consideração que as imagens adicionadar a um arquivo HTML, quando renderizadas, acabam ficando uma ao lado da outra, por isso, é necessário que use `<br>` para a quebra de página.

<!--Falar de listas numeradas e não numeradas-->

 `<div> Conteúdo </div>` | `<span> Conteúdo </span>` |
 |-----------------------|---------------------------|
 |Usada para definir uma divisão ou seção no documento, geralmente usada para agrupar elementos. O `<div>` é um elemento de bloco, o que significa que ele ocupa toda a largura disponível e começa em uma nova linha. | Usada para definir uma seção em linha, usada para agrupar elementos dentro de um parágrafo ou outro bloco de texto. O `<span>` é um elemento em linha, o que significa que ele não inicia uma nova linha e ocupa apenas a largura necessária para seu conteúdo.|

### Explicação das tags:

- **`<div>`**:
  - A tag `<div>` é usada como um contêiner genérico para agrupar outros elementos HTML. É um elemento de bloco, o que significa que ele ocupa toda a largura disponível e começa em uma nova linha. 
  - É frequentemente usada para aplicar estilos CSS a um grupo de elementos ou para organizar o layout de uma página web.
  - Exemplo de uso:
    ```html
    <div>
      <h1>Título</h1>
      <p>Este é um parágrafo dentro de um div.</p>
    </div>
    ```

- **`<span>`**:
  - A tag `<span>` é usada para agrupar partes de texto ou outros elementos em linha. É um elemento em linha, o que significa que ele não inicia uma nova linha e ocupa apenas a largura necessária para seu conteúdo.
  - É comumente usada para aplicar estilos CSS a uma parte específica de texto ou para manipulação via JavaScript.
  - Exemplo de uso:
    ```html
    <p>Este é um <span style="color: red;">texto destacado</span> dentro de um parágrafo.</p>
    ```

### Explicação das tags de formatação de texto:

- **`<b>`**:
  - A tag `<b>` é usada para deixar o texto em negrito. Essa tag não adiciona importância ao texto.
  - Exemplo:
    ```html
    <b>Texto em negrito</b>
    ```
    <b>Texto em negrito</b>

- **`<strong>`**:
  - A tag `<strong>` é usada para dar ênfase forte ao texto, geralmente exibido em negrito. Essa tag indica que o texto é de grande importância.
  - Exemplo:
    ```html
    <strong>Texto com ênfase forte</strong>
    ```
    <strong>Texto com ênfase forte</strong>

- **`<i>`**:
  - A tag `<i>` é usada para deixar o texto em itálico. Essa tag não adiciona ênfase ao texto.
  - Exemplo:
    ```html
    <i>Texto em itálico</i>
    ```
    <i>Texto em itálico</i>

- **`<em>`**:
  - A tag `<em>` é usada para dar ênfase ao texto, geralmente exibido em itálico. Essa tag indica que o texto deve ser enfatizado.
  - Exemplo:
    ```html
    <em>Texto com ênfase</em>
    ```
    <em>Texto com ênfase</em>

- **`<u>`**:
  - A tag `<u>` é usada para sublinhar o texto.
  - Exemplo:
    ```html
    <u>Texto sublinhado</u>
    ```
    <u>Texto sublinhado</u>

- **`<s>`**:
  - A tag `<s>` é usada para riscar o texto, indicando que algo foi deletado ou não é mais relevante.
  - Exemplo:
    ```html
    <s>Texto tachado</s>
    ```
    <s>Texto tachado</s>

- **`<mark>`**:
  - A tag `<mark>` é usada para destacar o texto com um fundo amarelo, como se tivesse sido marcado com um marcador.
  - Exemplo:
    ```html
    <mark>Texto destacado</mark>
    ```
    <mark>Texto destacado</mark>

- **`<small>`**:
  - A tag `<small>` é usada para exibir o texto em tamanho menor, muitas vezes usado para notas de rodapé ou avisos legais.
  - Exemplo:
    ```html
    <small>Texto menor</small>
    ```

- **`<sub>`**:
  - A tag `<sub>` é usada para exibir o texto em subscrito, abaixo da linha base, geralmente para fórmulas químicas ou matemáticas.
  - Exemplo:
    ```html
    H<sub>2</sub>O
    ```
    H<sub>2</sub>O

- **`<sup>`**:
  - A tag `<sup>` é usada para exibir o texto em sobrescrito, acima da linha base, geralmente para expoentes ou referências.
  - Exemplo:
    ```html
    E = mc<sup>2</sup>
    ```
    E = mc<sup>2</sup>

- **`<code>`**:
  - A tag `<code>` é usada para exibir o texto em uma fonte monoespaçada, geralmente para indicar um trecho de código.
  - Exemplo:
    ```html
    <code>console.log('Olá, mundo!');</code>
    ```

    <code>console.log('Olá, mundo!');</code>

- **`<pre>`**:
  - A tag `<pre>` é usada para exibir o texto em uma fonte monoespaçada, preservando espaços e quebras de linha, ideal para blocos de código.
  - Exemplo:
    ```html
    <pre>
    function hello() {
        console.log('Olá, mundo!');
    }
    </pre>
    ```
    <pre>
    function hello() {
        console.log('Olá, mundo!');
    }
    </pre>

- **`<blockquote>`**:
  - A tag `<blockquote>` é usada para indicar uma citação em bloco, geralmente recuada.
  - Exemplo:
    ```html
    <blockquote>
      Este é um exemplo de uma citação longa em bloco.
    </blockquote>
    ```

    <blockquote>
      Este é um exemplo de uma citação longa em bloco.
    </blockquote>

#### `<body>`
- **Descrição**: A tag `<body>` contém todo o conteúdo de um documento HTML, incluindo texto, imagens, links, etc.
- **Atributos Comuns**:
  - **Global attributes**: `class`, `id`, `style`, `title`, etc.

#### `<nav>`
- **Descrição**: A tag `<nav>` contém links de navegação.
- **Atributos Comuns**:
  - **Global attributes**: `class`, `id`, `style`, `title`, etc.

#### `<a>`
- **Descrição**: A tag `<a>` define um hyperlink, que é usado para vincular de uma página para outra.
- **Atributos**:
  - **`href`**: Especifica a URL da página a ser vinculada.
  - **`target`**: Especifica onde abrir o link (ex: `_blank` para abrir em nova aba).
  - **`rel`**: Define a relação entre o documento atual e o documento vinculado (ex: `noopener`, `noreferrer`).
  - **`alt`**: Alternativo textual da imagem.

#### `<img>`
- **Descrição**: A tag `<img>` é usada para incorporar uma imagem em uma página HTML.
- **Atributos**:
  - **`src`**: Especifica o caminho da imagem.
  - **`alt`**: Fornece um texto alternativo para a imagem.
  - **`height`** e **`width`**: Especificam a altura e a largura da imagem.

#### `<ul>`
- **Descrição**: A tag `<ul>` define uma lista não ordenada.
- **Atributos Comuns**:
  - **Global attributes**: `class`, `id`, `style`, `title`, etc.

#### `<li>`
- **Descrição**: A tag `<li>` define um item em uma lista (ordenada ou não ordenada).
- **Atributos Comuns**:
  - **Global attributes**: `class`, `id`, `style`, `title`, etc.

#### `<aside>`
- **Descrição**: A tag `<aside>` é usada para conteúdo relacionado tangencialmente ao conteúdo principal.

<br>

- **Atributos Comuns**:

  > **Global attributes**: `class`, `id`, `style`, `title`, etc.

#### `<figcaption>`
- **Descrição**: A tag `<figcaption>` define uma legenda para o conteúdo da `<figure>`.
- **Atributos Comuns**:
  - **Global attributes**: `class`, `id`, `style`, `title`, etc.

### Atributos Globais

Todas as tags mencionadas podem ter os seguintes atributos globais:

- **`class`**: Define uma ou mais classes CSS para o elemento.
- **`id`**: Define um identificador único para o elemento.
- **`style`**: Define estilos inline para o elemento.
- **`title`**: Define um título adicional para o elemento, frequentemente exibido como um tooltip.

`<table>`
Descrição: Define uma tabela.
Atributos:
border: Especifica a largura da borda da tabela.

`<thead>`
Descrição: Agrupa o conteúdo do cabeçalho de uma tabela.
Atributos Comuns:
Global attributes: class, id, style, title, etc.

`<tr>`
Descrição: Define uma linha em uma tabela.
Atributos Comuns:
Global attributes: class, id, style, title, etc.

`<th>`
Descrição: Define uma célula de cabeçalho em uma tabela.
Atributos:
Global attributes: class, id, style, title, etc.
rowspan: Especifica o número de linhas que uma célula de cabeçalho abrange.
colspan: Especifica o número de colunas que uma célula de cabeçalho abrange.

`<tbody>`
Descrição: Agrupa o conteúdo do corpo de uma tabela.
Atributos Comuns:
Global attributes: class, id, style, title, etc.

`<td>`
Descrição: Define uma célula em uma tabela.
Atributos:
Global attributes: class, id, style, title, etc.
rowspan: Especifica o número de linhas que uma célula abrange.
colspan: Especifica o número de colunas que uma célula abrange.

`<img>`
Descrição: Incorpora uma imagem em uma página HTML.
Atributos:
src: Especifica o caminho da imagem.
alt: Fornece um texto alternativo para a imagem.
height e width: Especificam a altura e a largura da imagem.

A tag `<input>` em HTML é um dos elementos mais versáteis, usada para criar uma variedade de campos interativos em formulários. Aqui está uma descrição detalhada de todos os atributos que podem ser usados com a tag `<input>`, especialmente quando especificamos diferentes tipos usando o atributo `type`.

### Atributos Comuns de `<input type="...">`

1. **`type`**
   - **Descrição**: Especifica o tipo de controle de entrada.
   - **Valores Comuns**:
     - `text`, `password`, `email`, `number`, `date`, `time`, `checkbox`, `radio`, `submit`, `reset`, `button`, `file`, `hidden`, `image`, `search`, `url`, `tel`, `color`, etc.

2. **`id`**
   - **Descrição**: Define um identificador único para o controle.

3. **`name`**
   - **Descrição**: Especifica o nome do controle, usado para identificar os dados do controle ao enviar o formulário.

4. **`value`**
   - **Descrição**: Define o valor inicial do controle. Este valor é enviado com o formulário.

5. **`placeholder`**
   - **Descrição**: Fornece uma dica ao usuário sobre o que pode ser inserido no controle (aplica-se a `text`, `search`, `url`, `tel`, `email`, `password`).

6. **`required`**
   - **Descrição**: Indica que o controle deve ser preenchido antes de enviar o formulário.

7. **`disabled`**
   - **Descrição**: Desabilita o controle, tornando-o não interativo.

8. **`readonly`**
   - **Descrição**: Torna o controle somente leitura (aplica-se a `text`, `search`, `url`, `tel`, `email`, `password`, `number`, `date`, `time`).

9. **`maxlength`**
   - **Descrição**: Especifica o número máximo de caracteres que o usuário pode inserir (aplica-se a `text`, `search`, `url`, `tel`, `email`, `password`).

10. **`minlength`**
    - **Descrição**: Especifica o número mínimo de caracteres que o usuário deve inserir (aplica-se a `text`, `search`, `url`, `tel`, `email`, `password`).

11. **`size`**
    - **Descrição**: Especifica o número de caracteres visíveis (aplica-se a `text`, `search`, `tel`, `url`, `email`, `password`).

12. **`pattern`**
    - **Descrição**: Define uma expressão regular que o valor do controle deve corresponder (aplica-se a `text`, `search`, `url`, `tel`, `email`, `password`).

13. **`min`**
    - **Descrição**: Especifica o valor mínimo permitido (aplica-se a `number`, `range`, `date`, `datetime-local`, `month`, `time`, `week`).

14. **`max`**
    - **Descrição**: Especifica o valor máximo permitido (aplica-se a `number`, `range`, `date`, `datetime-local`, `month`, `time`, `week`).

15. **`step`**
    - **Descrição**: Especifica o incremento numérico dos valores permitidos (aplica-se a `number`, `range`, `date`, `datetime-local`, `month`, `time`, `week`).

16. **`multiple`**
    - **Descrição**: Permite que o usuário selecione mais de um valor (aplica-se a `email` e `file`).

17. **`accept`**
    - **Descrição**: Especifica o tipo de arquivos que o controle de entrada de arquivos (`file`) deve aceitar (por exemplo, `accept="image/*"`).

18. **`checked`**
    - **Descrição**: Indica que o controle está marcado por padrão (aplica-se a `checkbox` e `radio`).

19. **`alt`**
    - **Descrição**: Define um texto alternativo para a imagem se o tipo for `image`.

20. **`src`**
    - **Descrição**: Especifica o URL da imagem a ser exibida, se o tipo for `image`.

21. **`autocomplete`**
    - **Descrição**: Define se o navegador deve tentar completar automaticamente os valores inseridos pelo usuário (valores: `on`, `off`).

22. **`autofocus`**
    - **Descrição**: Define que o controle deve receber o foco automaticamente ao carregar a página.

23. **`form`**
    - **Descrição**: Associa o controle a um ou mais formulários.

24. **`formaction`**
    - **Descrição**: Define a URL para onde os dados do formulário devem ser enviados (aplica-se a `submit` e `image`).

25. **`formenctype`**
    - **Descrição**: Define como os dados do formulário devem ser codificados ao serem enviados ao servidor (aplica-se a `submit` e `image`).

26. **`formmethod`**
    - **Descrição**: Especifica o método HTTP (`GET` ou `POST`) a ser usado ao enviar o formulário (aplica-se a `submit` e `image`).

27. **`formnovalidate`**
    - **Descrição**: Desativa a validação do formulário ao enviar (aplica-se a `submit` e `image`).

28. **`formtarget`**
    - **Descrição**: Especifica onde exibir a resposta após enviar o formulário (aplica-se a `submit` e `image`).

### Exemplos Práticos de Uso:

1. **Texto Simples**:
    ```html
    <input type="text" id="username" name="username" placeholder="Enter your username" required>
    ```

2. **Senha**:
    ```html
    <input type="password" id="password" name="password" required>
    ```

3. **Email**:
    ```html
    <input type="email" id="email" name="email" placeholder="you@example.com" required>
    ```

4. **Número**:
    ```html
    <input type="number" id="quantity" name="quantity" min="1" max="10" step="1">
    ```

5. **Data**:
    ```html
    <input type="date" id="birthday" name="birthday">
    ```

6. **Hora**:
    ```html
    <input type="time" id="appt" name="appt">
    ```

7. **Cor**:
    ```html
    <input type="color" id="favcolor" name="favcolor" value="#ff0000">
    ```

8. **Arquivo**:
    ```html
    <input type="file" id="myfile" name="myfile" accept=".jpg,.jpeg,.png,.pdf">
    ```

9. **Checkbox**:
    ```html
    <input type="checkbox" id="subscribe" name="subscribe" checked>
    ```

10. **Radio**:
    ```html
    <input type="radio" id="male" name="gender" value="male">
    <input type="radio" id="female" name="gender" value="female">
    ```

11. **URL**:
    ```html
    <input type="url" id="website" name="website" placeholder="https://example.com">
    ```

12. **Submit**:
    ```html
    <input type="submit" value="Submit">
    ```

13. **Reset**:
    ```html
    <input type="reset" value="Reset">
    ```

14. **Hidden**:
    ```html
    <input type="hidden" id="userid" name="userid" value="12345">
    ```

Essa descrição cobre a maioria dos atributos que podem ser usados com a tag `<input>` em diferentes tipos, proporcionando uma ampla flexibilidade para criar formulários interativos e úteis.

##### Lista de comandos HTML:

> `<!-- *conteudo * -->` | Usado para acrescentar comentários no código que não aparecerão para o usuário final.

> `<button> *Conteudo * </button>` | Usada para colocar um botão

> `<p> *Conteudo * </p>` | Usada para criar um parágrafo

> `<h1> Conteúdo </h1>` | Usada para representar um título de nível 1, geralmente usado como o título principal da página, mas que pode ir de 1 a 6.

> `<p> Conteúdo </p>` | Usada para criar um parágrafo de texto.

> `<div> Conteúdo </div>` | Usada para definir uma divisão ou seção no documento, geralmente usada para agrupar elementos.

> `<a href="URL">` Conteúdo </a> | Usada para criar um hiperlink que direciona para outra página ou parte da mesma página.

> `<span>` | Usada para definir uma seção em linha, usada para agrupar elementos dentro de um parágrafo ou outro bloco de texto.

> `<table>` | Usada para definir uma tabela de dados.

> `<ul> ` | Usada para definir uma lista não ordenada (com marcadores).

> `<ol>` | Usada para definir uma lista ordenada (numerada).

> `<li>` | Usada para definir um item de lista, dentro de uma `<ul>` ou `<ol>`.

> `<img src="URL" alt="Descrição">` | Usada para definir uma imagem. O atributo src especifica o caminho da imagem e o atributo alt fornece um texto alternativo.

> `<br>` | Usada para quebrar a linha, ou dar espaçamento entre linhas dentro de um arquivo.

>`<hr>` | Usado para criar uma linha horizontal

> `<div>` | Usada para definir uma divisão ou seção no documento, geralmente usada para agrupar elementos

> `<span>` | Usada para definir uma seção em linha, usada para agrupar elementos dentro de um parágrafo ou outro bloco de texto

> `<header>` | Usado para criar o cabeçalho de uma página

> `<main>` | Usado como conteiner para o conteudo principal da página

> `<footer>` | Usado para criar o rodapé de uma página

- Lista de comandos de formatação de texto em HTML: 

> `<b> Conteúdo </b>` | Usada para deixar o texto em negrito.

> `<strong> Conteúdo </strong>` | Usada para dar ênfase forte ao texto, geralmente exibido em negrito.

> `<i> Conteúdo </i>` | Usada para deixar o texto em itálico.

> `<em> Conteúdo </em>` | Usada para dar ênfase ao texto, geralmente exibido em itálico.

> `<u> Conteúdo </u>` | Usada para sublinhar o texto.

> `<s> Conteúdo </s>` | Usada para riscar o texto (strike-through).

> `<mark> Conteúdo </mark>` | Usada para destacar o texto com um fundo amarelo.

> `<small> Conteúdo </small>` | Usada para exibir o texto em tamanho menor.

> `<sub> Conteúdo </sub>` | Usada para exibir o texto em subscrito (abaixo da linha base).

> `<sup> Conteúdo </sup>` | Usada para exibir o texto em sobrescrito (acima da linha base).

> `<code> Conteúdo </code>` | Usada para exibir o texto em uma fonte monoespaçada, geralmente para código.

> `<pre> Conteúdo </pre>` | Usada para exibir o texto em uma fonte monoespaçada, preservando espaços e quebras de linha.

> `<blockquote> Conteúdo </blockquote>` | Usada para indicar uma citação em bloco.

### CSS

### Cores

#### Propriedades de Cor

- **`color`**: Define a cor do texto de um elemento.
  ```css
  p {
    color: blue;
  }
  ```

- **`background-color`**: Define a cor de fundo de um elemento.
  ```css
  div {
    background-color: yellow;
  }
  ```

### Formatos de Cor

- **Nomes de Cores**: ex. `red`, `blue`, `green`.
- **Hexadecimal**: ex. `#ff0000` (vermelho).
- **RGB**: ex. `rgb(255, 0, 0)` (vermelho).
- **RGBA**: ex. `rgba(255, 0, 0, 0.5)` (vermelho com 50% de opacidade).
- **HSL**: ex. `hsl(0, 100%, 50%)` (vermelho).
- **HSLA**: ex. `hsla(0, 100%, 50%, 0.5)` (vermelho com 50% de opacidade).

## Background

### Propriedades de Background

- **`background`**: Atalho para definir todas as propriedades de fundo em uma única linha.
  ```css
  body {
    background: #ffffff url('bg.jpg') no-repeat fixed center;
  }
  ```

- **`background-image`**: Define uma imagem de fundo para um elemento.
  ```css
  header {
    background-image: url('header-bg.jpg');
  }
  ```

- **`background-repeat`**: Define se e como a imagem de fundo será repetida.
  ```css
  section {
    background-repeat: no-repeat;
  }
  ```

- **`background-position`**: Define a posição da imagem de fundo.
  ```css
  footer {
    background-position: center bottom;
  }
  ```

- **`background-size`**: Define o tamanho da imagem de fundo.
  ```css
  aside {
    background-size: cover;
  }
  ```

- **`background-attachment`**: Define se a imagem de fundo é fixa ou rola com a página.
  ```css
  article {
    background-attachment: fixed;
  }
  ```

## Edição de Texto

### Propriedades de Texto

- **`font-family`**: Define a família de fontes do texto.
  ```css
  h1 {
    font-family: 'Arial', sans-serif;
  }
  ```

- **`font-size`**: Define o tamanho da fonte.
  ```css
  p {
    font-size: 16px;
  }
  ```

- **`font-weight`**: Define a espessura da fonte.
  ```css
  strong {
    font-weight: bold;
  }
  ```

- **`font-style`**: Define o estilo da fonte (normal, itálico, oblíquo).
  ```css
  em {
    font-style: italic;
  }
  ```

- **`text-align`**: Define o alinhamento do texto (left, right, center, justify).
  ```css
  div {
    text-align: center;
  }
  ```

- **`text-decoration`**: Define a decoração do texto (underline, overline, line-through, none).
  ```css
  a {
    text-decoration: none;
  }
  ```

- **`line-height`**: Define a altura da linha.
  ```css
  p {
    line-height: 1.5;
  }
  ```

- **`letter-spacing`**: Define o espaçamento entre caracteres.
  ```css
  h1 {
    letter-spacing: 2px;
  }
  ```

- **`text-transform`**: Define a capitalização do texto (uppercase, lowercase, capitalize).
  ```css
  h2 {
    text-transform: uppercase;
  }
  ```

- **`text-shadow`**: Adiciona sombra ao texto.
  ```css
  h3 {
    text-shadow: 2px 2px 5px grey;
  }
  ```

---

Este resumo cobre as principais propriedades relacionadas a cores, background e edição de texto em CSS, juntamente com exemplos de como usá-las.


## Teste de aptidão
### Resultado
## Resolução de caso
## Coding tank
