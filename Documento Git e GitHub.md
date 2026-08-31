# Documento para prova 1 (Git e GitHub)
Neste documento iremos ver sobre algumas funcionalidades do git,o que é branch, como funciona e no meio irei mostrar toda a minha raiva ao programar.

Para usar os códigos do Git você estará usando o terminal ou sistema de programação de sua preferência
Mas antes, 
## Por que eu usaria o Git?
O git ele tem uma função, a função de **guardar seus programas anteriores**, para que possa rever eles, ou até **retornar a eles em caso de algum erro** ter acontecido. 
Além desse uso podemos **criar ramos no nosso código**, para que possamos codar coisas diferentes, sem que o código principal seja afetado, para no futuro uni-los novamente.
Outra funcionalidade é o **compartilhamento dos seus códigos**, visto que com o git você não terá que copiar seu código inteiro e enviar por whats para o seu amigo, precisando agora apenas mandar o link do repositório do GitHub



Dado que está aprendendo agora a primeira coisa que temos que aprender é

## Git init
O **Git init** tem como objetivo **inicializa o Git dentro de uma pasta**, criando um arquivo sem nome em uma pasta do seu computador

Importante frisar que o Git int **não cria um repositório no GitHub**.

### Como escrever:
```
Git init
```
caso isso seja feito você verá um novo arquivo no seu computador chamado 

> `.git/`

indo disso:
```
meu-projeto/ 
	├── main.py 
		└── README.md
`````

Para isso
```
meu-projeto/ 
	├── .git/
	├── main.py 
		└── README.md
```
### O que pode ser feito junto dele?

Um dos complemento que podemos adicionar ao Git init é o nome para o arquivo, que estaremos fazendo o Git, para fazer isso fazemos da seguinte forma:

```git
git init nome.projeto
```

Com isso criaremos um novo arquivo que dentro desse arquivo fará o seu versionamento e salvamento para o GitHub.

Caso queira nomear a sua branch, para saber qual se é a principal, ou só uma de complemento, você pode usar -b para nomear a branch, ficando assim:

```
Git init -b main
```

Com isso na pasta que você está você terá o Git iniciado e a branch que pediu.

## Git status
O **Git status** ele te dará um **geral sobre a sua Branch atual**, sendo alguns desses status a branch que você está, se você já salvou algum projeto (deu algum commit) e diz quais arquivos vão ser salvou ou não quando der commit.

### Como escrever:
```
Git status
```
caso isso seja feito aparecerá um prompt, indo pela ideia que estamos na mainpy, aparecerá o seguinte prompt

```
On branch main #qual a branch

No commits yet #se já foi feito commit

Untracked files: #não será salvo no commit
  main.py
```

### O que pode ser feito junto dele?
Você pode simplificar ou filtrar algumas das informações que o Git status mostrará, aqui alguns desses exemplos:

#### Git status -s ou Git status --short
Com esse comando o prompt de status será simplificado aparecendo assim:
```
 M main.py
?? teste.py
```
Os símbolos
```
 M   → arquivo modificado, mas não colocado no staging
M    → arquivo modificado e colocado no staging
??   → arquivo não rastreado (Untracked)
```

### Git status -b
Com esse comando ele mostrará a branch atual e de forma resumida assim:
```
## main
 M main.py
?? teste.py
```

## Git add
Quando usado o **Git add** você está **salvando uma parte para ser alterada, basicamente colocando na lista de espera** para o commit. 

### Como escrever:
```
Git add main.py
```
Depois de dar add imagine essa ação como uma lista:
```
Lista de para commit:
- main.py
```
E caso queira adicionar mais algum arquivo basta fazer mais um Git add
```
Git add calculadora.py
```
Depois de dar add:
```
Lista de para commit:
- main.py
- calculadora.py
```

### O que pode ser feito junto dele?
Você pode adicionar mais de 1 arquivo ao mesmo tempo
```
Git add main.py calculadora.py
```
#### Git add .

Outra forma de colocar mais de 1 arquivo na "fila" é com "git add ." com isso todos os arquivos da pasta e subpastas serão adicionadas a lista para serem salvas (ou commitadas)

```
Git add .
```
#### Git add *.(documento)

Também podemos escolher arquivos de um tipo especifico para serem adicionados.
```
git add *.py
```
Neste exemplo estamos adicionando apenas arquivos em python.

#### Git add -p
Com esse podemos salvar partes especificas das alterações do arquivo

## Git commit
Este é o comando que **salvará todas as suas alterações** que você adicionou com o add.

### Como escrever:
```
Git commit
```
Quando feito isso você estará salvando no seu computador o histórico dos seus códigos.
Algo recomendado para fazer junto do git commit é deixar uma mensagem, para facilitar a navegação atrás de alguma versão antiga sua. O código para isso é o seguinte:
```
Git commit -m "sistema de registro"
```
Quando usar o git log, verá um código e a mensagem que você escreveu


### O que pode ser feito junto dele?

#### Git commit --amend
Com esse código você salvará o seu ultimo commit, sem ter que salvar uma nova versão.

#### Git commit --amend  --no-edit
Com esse código você fará o mesmo que o código anterior, mas mantendo o nome da versão

#### Git commit -v
Ao usar **-v** você verá as diferenças das alterações enquanto você está preparando a mensagem do commit.
Pode ser útil para revisar exatamente o que está prestes a ser registrado.

## Git log
Quando usado **receberá um registro de todos os commits já feitos** 

### Como escrever:
```
Git log
```
Quando escrito receberá uma mensagem similar com essa aqui:
```
commit 8f31a2c...
Author: Fabricio
Date:   ...

    Esquema de bets

commit 42bd91e...
Author: Fabricio
Date:   ...

    sistema de registro

commit a73c812...
Author: Fabricio
Date:   ...

    Cria projeto
```


### O que pode ser feito junto dele?

#### Git log --oneline
Com esse código você receberá um registro mais simples, ele se parecerá assim:

```
8f31a2c Esquema de bets
42bd91e Sistema de registro
a73c812 Cria projeto
```

#### Git log --oneline --graph
Isso mostrará visualmente como as linhas de desenvolvimento se ramificaram ficando assim:
```
* 91ab234 Adiciona login
|\
| * 72cd891 Cria formulário
|/
* 42bd91e Cria projeto
```
#### git log -p
Ele mostra o que foi alterado, ou seja, exatamente quais linhas foram adicionadas e removidas em cada commit.

Por exemplo, você pode ver algo como:

```
- print("Olá")
+ print("Olá, mundo!")
```

## Git branch
Esse é o comando relacionado às **branches (ramificações)** do Git. Com ele você cria essas ramificações, para poder desenvolver códigos fora da sua main, e pode ver em qual branch está trabalhando no momento.

### Como escrever:
O Git branch tem duas formas de ser usado

```
Git branch
```
Com esse código será mostrado em qual branch você está trabalhando, ficando com um asterisco na frente dela, assim:
```
* main
  outra_branch
```
Outra variação do Git branch é o:
```
Git branch Nova_branch
```
Aqui você estará criando uma nova branch, no entanto você não irá mudar para ela, tendo assim que mudar manualmente para ela com **Git checkout** ou **Git switch**.
 
### O que pode ser feito junto dele?

#### Git Branch -m
Com esse código, você renomeia-rá a sua branch atual. Exemplo:
```
Git branch
```
```
* master
```
```
Git branch -m main
Git branch
```
```
* main
```
## Git switch
Com esse comando é possível **transitar entre as branchs**

### Como escrever:
```
Git switch (funcão_desejada)
```
ao rodar o código você sairá da branch atual direto para a branch que você escreveu
```
* main
  funcão_desejada
```
```
  main
* funcão_desejada
```
### O que pode ser feito junto dele?
#### Git switch -c (funcão_desejada)
Provavelmente uma das sintaxe mais interessantes, pois com ela você cria uma branch nova e já move pra ela, podendo codar nela imediatamente.

```
Git switch -c (funcão_desejada)
```

## Git Checkout
Dos comandos existentes esse é um dos mais antigos, mas que ainda pode ser usado. Ele é um comando multifuncional, **podendo criar uma branch, trocar para uma branch, analisar um antigo commit e até restaurar um arquivo**, coisas que podem ser feitas com outros comandos mais específicos.

### Como escrever:
#### Para trocar:
```
git checkout branch_existente
```
Com esse comando você irá trocar para a branch já existente, exatamente como o git switch faria.

#### Para criar e entrar em branch:
```
git checkout -b branch_nova
```
Aqui você irá criar uma branch e no mesmo instante trocará para ela, assim como um git switch -c faria

#### Para ver antigos commits:
```
git checkout código_do_commit
```
Com isso você poderá checar o estado que o projeto se encontrava na época. Isso não afetará nada, ajudando a ter uma ideia das coisas que você mudou ou não. 

#### Para restaurar arquivos:
```
git checkout -- main.py
```
Aqui você estará restaurando o seu arquivo main.py, algo que pode ser feito assim:
```
git restore main.py
``` 
Esses dois comando fazem a mesma coisa, mas o segundo é mais claro e simples.

## Git merge
Com o **Git merge** você consegue **unir duas branchs diferentes em uma só branch**
### Como escrever:
```
Git merge branch_desejada
```
Com isso a branch que você quer se juntará com a branch que você está no momento.

### O que pode ser feito junto dele?
#### Git merge --abort
Caso ocorra algum conflito com o merge ao usar esse comando  o git retornará o repertório para o estado antes do comando git merge.

## Git remote
Com o **Git remote** teremos a **conexão entre o repositório do nosso computador com o repositório remoto ou do GitHub**

### Como escrever:
```
git remote add origin URL_DO_REPOSITORIO
```
Com esse comando iremos mostrar qual o nosso repositório no GitHub, para que possamos enviar nossos commits para lá.
com o **add** sendo o nosso código para adicionar 

Em seguida podemos fazer um:
```
Git remote
e
Git remote -v
```
Para mostrar o endereço

## Git push
O **Git push** tem como principal função **enviar os commits para um repositório remoto**, como o GitHub

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTEwMzk4MTU0MCwtMTcwMjgxMzk5OSwtOD
c4MDQ3NzE1LDMxNjY0MzM4NCw0NDc1MjQ1MDMsNDA5NzY3NTM5
LDE2ODQxMDg3NSwtMTY1NjAxNTM5MCwtMTE2NzI4OTM4LC0xND
MzMDg1MTU3LC0yODIwNzAxMCwtNDk0MjA2MTczLDEyMzY0NTQ2
OTAsLTE2NDMyNDA2NTYsLTIwMzA2MDAxNF19
-->