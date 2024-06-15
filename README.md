# Ada - Santander Coders
## Curso online
### Caderno de anotações
#### Git e Versionamento
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

### Lista de comandos:
> git config --global user.name "nome do usuário" | Configura o nome do usuário daquela máquina

> git config --global user.email *email do usuário *| Configura o email do usuário daquela máquina

> git init | Inicia o git na pasta usada

> git add * nome do arquivo * | Passa o arquivo em questão de Modified para Staged 

> git commit -m "nome da atualização" | Faz o commit do arquivo, e passa ele de Staged para Unmodified

> git commit -am "nome da atualização" | Faz o commit de todos os arquivos que estão em estado de Modified sem precisar usar 'git add'

> git status |  Mostra o status do arquivo

> git diff | Mostra as alterações feitas no arquivo, quando está no status Modified

> git diff --staged | Mostra as alterações feitas no arquivo, quando está no status Staged
## Teste de aptidão
### Resultado
## Resolução de caso
## Coding tank
