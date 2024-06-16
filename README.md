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

##### Lista de comandos HTML:

> `<!-- *conteudo * -->` | Usado para acrescentar comentários no código que não aparecerão para o usuário final.

> `<button> *Conteudo * </button>` | Usada para colocar um botão

> `<p> *Conteudo * </p>` | Usada para criar um parágrafo

> `<h1> Conteúdo </h1>` | Usada para representar um título de nível 1, geralmente usado como o título principal da página, mas que pode ir de 1 a 6.

> `<p> Conteúdo </p>` | Usada para criar um parágrafo de texto.

> `<div> Conteúdo </div>` | Usada para definir uma divisão ou seção no documento, geralmente usada para agrupar elementos.

> `<a href="URL">` Conteúdo </a> | Usada para criar um hiperlink que direciona para outra página ou parte da mesma página.

> `<span> Conteúdo </span>` | Usada para definir uma seção em linha, usada para agrupar elementos dentro de um parágrafo ou outro bloco de texto.

> `<table> Conteúdo </table>` | Usada para definir uma tabela de dados.

> `<ul> Conteúdo </ul>` | Usada para definir uma lista não ordenada (com marcadores).

> `<ol> Conteúdo </ol>` | Usada para definir uma lista ordenada (numerada).

> `<li> Conteúdo </li>` | Usada para definir um item de lista, dentro de uma `<ul>` ou `<ol>`.

> `<img src="URL" alt="Descrição">` | Usada para definir uma imagem. O atributo src especifica o caminho da imagem e o atributo alt fornece um texto alternativo.

> `<br>` | Usada para quebrar a linha, ou dar espaçamento entre linhas dentro de um arquivo.

>`<hr>` | Usado para criar uma linha horizontal

## Teste de aptidão
### Resultado
## Resolução de caso
## Coding tank
