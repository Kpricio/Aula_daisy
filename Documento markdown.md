# Documento para prova 1 (markdown)

## Para o que serve o marketing?
ele é um instrumento de trabalho muito útil para a documentação de coisas, especialmente para trabalhos que tem programação 

## Quais são algumas das funcionalidades do markdown

### Títulos
Para fazer títulos utilizamos o # para isso e a quantidade de hashtag determinará o tamanho do titulo, quanto menos hashtag maior será o título.
Exemplos
# Título 
## Subtítulo 

###### subsubsubtitulo 

## Formatação 
Na hora de escrever podemos deixar as palavras ou frases de diversas formas, seja em _italico_ usando 1 " _ " ou " * ", podemos deixar __negrito__ com dois  " _ " ou " * " e até mesmo ~~taxado~~ com dois " ~ ".
Também é possivel fazer ==marcações== para destacar mensagens, usando " = ".
Com " \_ "é você consegue colocar pequenas barras nos cantos da \_frase ou palavra\_

Além dessa forma de formatação, podemos também usar <> com um letra no meio, aqui vão exemplos:
<p><q> Com o <q>q</q> podemos colocar aspas em frases e palavras.</q></p>
<p><u> Com o <q>u</q> podemos sublinhar frases e palavras. </u></p>
<p><i> Utilizando <q>i</q> deixamos a frase/palavras.</i></p>
<p> Caso queira pular uma linha podemos usar <q>p</q> para isso.</p>
<p><a> Também é possível deixar o texto/palavra azul e sublinhada com <q>a</q>.</a></p>
<p><s> Podemos rasurar palavras com o <q>s</q> também.</s></p>
<p><b> Para deixar em negrito usasse o <q>b</q>.</p>


## Listas
Existem diversos tipos de listas, aqui vão alguns exemplos:
- Esse tipo de lista usa um " - " para começar a lista
* Já esse utiliza um " * " para começar a lista
1. Também podemos fazer listas numeradas

Além dessas três formas de lista podemos criar listas com espaços, ficando assim
- Primeira parte
	- Segunda parte, apertando TAB para criar isso
		- terceira parte, fazendo o mesmo que no caso anterior

## Nota de rodapé
Notas de rodapé estão aqui para ajudar com pequenas ajudas  ou informações interessantes e essa é a sintaxe:
[^1]Clica aqui vai
[^2]Se funcionou clica aqui por favor

[^1]:Vai toma no teu cu
[^2]:Já parou pra pensar que nota de rodapé parece uma nota por alguém ter rodado o pé

## Links e imagens
Neste setor iremos ver todas as formas de colocar links, imagens e como modifica-las

Começando pelo link, para adicionar um link usamos a seguinte sintaxe:

[texto do link](Link da pagina)

exemplo:

[Material para esse documento](https://ufprvirtual.ufpr.br/pluginfile.php/2915184/mod_resource/content/1/Mo%CC%81dulo_01.pdf)

Outra coisa possível é de colocar uma imagem e essa é a sintaxe:
![texto do link](Link da imagem)

Exemplo:

![naoaguentomais](https://images.pexels.com/photos/7531979/pexels-photo-7531979.jpeg)

Mas além desses dois, podemos também junta-los e fazer uma imagem que ao clicar leva para uma pagina
A sintaxe para isso é a seguinte
[![texto do link](Link da imagem)](Link da pagina)

Exemplo:

[![hahahahah](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQQPYoWBx7DSa_CmzWXTpxn5q0a5yX9qvag2sTg-lD_ha1NaIQ_2ScBQiKCXxu6N0vDn-rLqqisnp08L4OlSP8oIFk99BEG3p-HhNe83eeD5Q&s=10)](https://www.youtube.com/watch?v=8_MHhwQ4LJA)
==<b> click na imagem</b>==

## Bloco de código
Neste setor veremos como mostrar linhas de código e o que podemos fazer em outros markdowns.

Para criar uma linha de código usamos uma crase/assento, ficando assim:

 `Print("hello world")`
 `Print("hello world")
 Print("hello world")
 Print("hello world")`

com apenas uma crase o seu código será mostrado em uma linha como é mostrado a cima, mas também podemos usar três crase/assento para criar um blobo de código

```
Print("hello world")
```
 ```
 Print("hello world")
 Print("hello world")
 Print("hello world")
 ```
Algo que podemos fazer é falar qual  tipo de código é o bloco de texto, usando a seguinte sintaxe:

```r
x <- 5
y <- 4
```

Esse uso também serve para extensões como a extensão mermaid.

## Tabelas
Muitas vezes teremos que mostrar nossos com uma tabela e a principal forma de fazer isso é com barras retas " | ", e fica assim:

| Coluna 1 | Coluna 2 |
|----------|----------|
| Dado 1 | Dado 2 |
| Dado 3 | Dado 4 |

Outro exemplo seria o seguinte
| |Blight| Murse| Trapper|
|---|----|---|---|
|Vitórias |0| 1|10000|
|Derrotas |Todas|Maioria|Nunca|

## Referencias e citações
Existem diversas formas de fazer uma referencia ou citação, podendo usar o já visto nota de rodapé, mas existem algumas outras formas de o fazer.
Uma dessas formas é utilizando o @ pra criar essa citação, com a sintaxe ficando [@Código].
Usar isso ficaria mais ou menos assim:
Segundo [@todososmeusamigos] "Eu te odeio Fabricio".

O uso do @ necessita de um documento para ser puxado para ser mostrado a referencia.
Mas existem outras formas de fazer um citação e uma dessas é com o " > ".

Caso use a seta a sua citação ficaria assim
> Estou sendo citado.

# E depois do básico?
Quando aprender as principais funções do markdown, você pode passar para as extenções que ele oferece, podendo criar 
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTEwNTYzMDUyMSwxMzQ0NDIyMTE0LDE2Nj
EzNDQ3OTVdfQ==
-->