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
Quando usado o **Git add** você está colo colosalvando uma parte para ser alterada, basicamente colocando na lista de espera para o commit. 

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
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTg0MDExNzI1OCwyMTM5NjQwMjIxLDEzNT
Q5MDY0MDYsLTQ5ODIzOTc0NSwzMTU2Mzg2OTYsLTg1ODA1MzY5
LC00NDA3MjE3MDQsOTgyNTY5Njk2LC03OTI0MjUzMSwtMTYwOT
kyODYxNSwtMTUzMTExOTkzNSwxNTAyNjk4MDMsMTUyMzk2MDU2
MF19
-->