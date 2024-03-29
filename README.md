# Documentacao_python
Documentação dos estudos de python

### Conceitos importantes:

* Programa:
  Um programa é uma sequência de instruções para executar operações de computação.

* Algoritmo:
  As sequências de instruções que criamos com fim de solucionar problemas são chamadas de algoritmo

### Início:
* **Hello world**

~~~python

print("Hello world")

~~~


* **Valores Inteiros, tipo _Int_**

~~~python
>>> 2
2
~~~

* **Valores flutuantes, tipo _float_**
~~~python
>>> 1.61
1.61
~~~

* **Valores tipo _String_**
~~~python
>>> "Hello world"
Hello world
>>> 'Hello world'
Hello world
~~~

* **Valores Booleanos**
~~~python
>>> True
True
>>> False
False
~~~

* **Variáveis**

Uma variável em Python é um nome que aponta para um valor. A instrução de dar um valor
  à variável é chamada de atribuição.
~~~python
>>> largura = 10

>>> largura * 2
20
~~~

  Uma vez criada uma variável, podemos substituir o valor que ela contém
    
~~~python
>>> distancia = 2
>>> distancia
2
>>> distancia = 5
>>> distancia
5
~~~
  PS: fique atento para escrever o nome da variável da mesma forma que ela foi criada,
  pois o Python difere maiúsculas de minúsculas, é CASE SENSITIVE, para o interpretador
  "distancia" e "Distancia" são duas variáveis diferentes.  

* **Nome das variáveis**

  Válido | Inválido | Por que é inválido?
  -------|----------|--------------------
  minha_string | minha-string | Hifens não são permitidos
  int4 | 4int | Não pode começar com número
  MINHA_CONST | $MINHA_CONST | Não pode usar símbolos diferentes de underline "_"
  largura_real | largura real | Não pode haver espaços

PS: também não podem ser dados nomes que a linguagem Python utiliza na sua sintaxe,
as chamadas palavras reservadas abaixo:
~~~python
and        del      from    not     while    
as         elif     global  or      with
assert     else     if      pass    yield
break      except   import  print
class      exec     in      raise
continue   finally  is      return
def        for      lambda  try
~~~

* **Operadores Aritméticos**

  Os operadores aritméticos básicos do Python são + , - , * , / e **
sendo, respectivamente soma, subtração, multiplicação, divisão e exponenciação
~~~python
>>> 1+2
3
>>> 10-3
7
>>> 21*2
42
>>> 5/2
2.5
>>> 10**2
100
~~~
  Além desses, também tem o operador módulo %, que retorna o resto da divisão, e o 
Floor Division //, o qual remove o valor decimal da divisão:
~~~python
>>> 2%2
0
>>> 3%2
1
>>> 3/2
1.5
>>> 3//2
1
~~~

* **Operações com Strings**

  Os operadores também podem ser usados com __strings__, ao somar duas __strings__
temos como resultado a união delas, chamada de concatenação.

~~~python
>>> "Python"+"Rocks"
PythonRocks
~~~
  
  Vejamos o que acontece ao somar uma __string__ com um inteiro.

~~~python
>>> "Python"+3
Traceback (most recent call last):
  File "<pyshell#0>" , line 1, in <module>
    "Python"+3
TypeError: must be str, not int
~~~

Obtemos um erro, pois apenas podemos somar **string** com **string**, e números com
números. Assim, para unir um número a uma **string** precisamos, antes, converter o 
número em uma **string** com a função **str**:

~~~python
>>>"Python"+str(3)
Python3
~~~

Da mesma forma, para obtermos uma soma númerica, não podemos utilizar diretamente
uma **string**, é necessário, antes, convertê-la em um tipo númerico. Essa conversão
de tipos é chamada _casting_. Para converter uma **string** para um inteiro utilizamos
a função **int** e para um **float** a função **float**.
~~~python
>>> int("20")+ 22
42
>>> float('2.5')+3
5.5
~~~

* **Comentários**

Os comentários são anotações inseridas no código para o próprio programador e são
ignorados pelor interpretador. São importantes para explicar para si mesmo e para os
outros o que determinado bloco de código faz.
O # é utilizado para comentar o conteúdo de uma linha.
Para comentar várias linhas pode-se utilizar as aspas triplas no início e no fim do comentário.
Abaixo apresento um código de cálculo de áreas com comentários elucidativos:

~~~python
# Cálculo da área de um círculo
raio = 4
pi = 3.14
print("área do círculo "+str(pi*raio**2))

""" Cálculo da área de um retângulo """
base = 2
largura = 3
print("área do retângulo "+str(base*largura))

área do círculo 50.24
área do retângulo 6
~~~

* **Input**

E se você quisesse obter os dados do usuário? Nesse caso, você pode utilizar a função input.
A referida função captura o dado do usuário e nos retorna esse valor em string
~~~python
entrada = input("Qual é o seu nome?")
print('Seu nome é ', entrada)

>>> Qual o seu nome?Matheus
Seu nome é Matheus
~~~

* **Função Len**

A função informa quantos elementos uma sequência tem quanto utilizada em uma __string__, nos 
dizendo quantos caracteres a **string** contém, veja:
~~~python
>>> len('Hello')
5
~~~

### Expressões condicionais

* **Expressões booleanas**

Para realizar decisões é necessário que antes saibamos comparar valores. As espressões booleanas
nos permitem fazer essa comparação e obter como resultado __True__ ou __False__
~~~python
>>> # Comparação de igualdade
>>> 3==3
True
>>> 3==4
False

>>> # Comparação de desigualdade
>>> 5!=5
False
>>> 5!=6
True

>>> # Comparação de maior que
>>> 5>2
True
~~~
Em resumo os operadores relacionais são:
Comparações | Significado
------------|------------
x == y | x igual a y
x != y | x diferente de y
x > y | x maior que y
x < y | x menor que y
x >= y | x maior ou igual a y
x <= y | x menor ou igual a y

* **Intrução If**

O __if__ é a forma mais elementar de avaliação. 
A expressão é avaliada pelo interpretador: se ela for verdadeira, 
o bloco interno ao **if** é executado, se não for verdadeira não é executado 
e nada seria impresso
~~~python
>>> nota = 8
>>> if nota => 7:
      print("Você passou")
Você passou
~~~
Em português a instrução seria: 
```
Se Verdadeiro:
  Comandos
```
* **Indentação**

O espaçamento à esquerda, logo abaixo da declaração __if__, não é apenas estético,
o Python utiliza os espaçamentos para delimitar os blocos de código, ou seja, é esse
espaçamento que expresssa que o __print__ está dentro do __if__. Em Python por convenção,
são utilizados quatro espaços para cada nível de bloco. Essa delimitação por espaços é chamada
de indentação! Quando uma indentação não é respeitada o interpretador acusará um erro.

* **Else**

Criaremos um script que verifica a senha de um usuário:
~~~python
>>> senha = input("Digite sua senha")
>>> if senha == "123oliveira4":
       print("Senha correta")
~~~
Muito bem, se for inserida a senha correta, obteremos a mensagem "Senha correta". Porém, caso
a senha esteja errada, nenhuma mensagem é enviada.

A cláusula __else__ é a alternativa que é executada caso o **if** seja avaliado como falso. Podemos
agora avisar se a senha estiver incorreta.
~~~python
>>> senha = input("Digite sua senha")
>>> if senha == "123oliveira4":
       print("Senha correta")
    else:
       print("Senha incorreta")
~~~

### Operadores Booleanos

* **And**

O operador __and__ avalia se dois valores ou expressões são verdadeiras, se ambos forem, o resultado é verdadeiro, caso 
contrário retorna o valor de falso. Em resumo, com o __and__ estamos perguntando: são ambas expressões verdadeiras?
~~~python
>>> 3==3 and 4>3
True
>>> True and True
True
>>> 2>10 and 5==5
False
>>> True and False
False
~~~

* **Or**

Já com o operador __or__, apenas um dos valores precisa ser verdadeiro. Estamos perguntando, algum dos valores é verdadeiro?
~~~python
>>> 2>10 or 5==5
True
>>> True or False
True
~~~

* **Not**

O operador __not__, simplesmente inverte o valor booleano
~~~python
>>> not True
False
>>> not False
True
~~~

### Expressões condicionais 2

* **Else if**

O **elif** nada mais é que um **else** seguido de um **if**. Por exemplo, vamos criar um
sistema de classificação para um jogo:
~~~python
pontuacao = 75
if pontuacao <= 50:
   print("newba")
elif 50 < pontuacao <=70:
   print("mediano")
elif 70 < pontuacao <=90:
   print("óia ele")
else:
   print("O escolhido")
~~~
OBS: ao utilizar o **elif** apenas uma das opções é executada, mesmo que as outras também
sejam condições válidas

Por exemplo, se quiséssemos avaliar se uma pessoa atenderia aos requisitos para ir a uma montanha russa
muito restrita, o **elif** não atenderia, pois ele apenas verifica se uma condição é válida, enquanto é necessário
que as três sejam também conferidas
~~~python
idade = 19
altura = 1.6
ticket_valido = True

if ticket_valido:
   print("Seu ticket é válido")
elif idade > 18:
   print("Você é maior de idade")
elif altura > 1.5:
   print("Altura permitida")
else:
   print("Requisitos não atendidos")
~~~
Podemos aninhas 'ifs' como uma solução, ou seja, colocar um **if** dentro do outro. Ou poderíamos também utilizar o **and**
~~~python
idade = 19
altura = 1.6
ticket_valido = True

if ticket_valido:
   print("Seu ticket é válido")
   if idade > 18 and altura > 1.5:
       print("Entrada permitida")
else:
   print("Requisitos não atendidos")
~~~

* **Utilizando valores no if**

O **if** avalia se o valor que o sucede é verdadeiro ou falso. Em Python não apenas expressões booleanas
resultam em verdadeiro ou falso, outros valores do Python também são avaliados da mesma maneira. Por exemplo,
o valor zero é avaliado em falso, os demais números em verdadeiro, uma **string** vazia é falsa, já uma com 
texto é verdadeira. Para avaliar se um valor resulta em verdadeiro ou falso utiliza-se a função **bool**:
~~~python
>>> bool("Matheus")
True
>>> bool("")
False
>>> bool(1)
True
~~~

A seguir, um exemplo que ilustra a utilização direta de valores no **if**:
~~~python
senha = input("Digite sua senha")

if senha:
   print("Senha válida")
else:
   print("A senha não pode estar em branco")
~~~

Observe que o **if** recebe o valor de uma **string** contida na variável "senha", se ela tiver o conteúdo
o **if** é verdadeiro, caso esteja vazia é avaliado como falso

* **Operador ternário**

O operador ternário é uma sintaxe para analisar expressão condicional de forma compacta em uma única linha:
~~~python
' se_verdadeiro if expressão else se_falso '

>>> umidade = 60
>>> "Úmido" if umidade >= 50 else "Seco"
Úmido
~~~

### PROJETO - A MÁGICA BOLA 8

Bola de adivinhação, contendo resultados aleatórios 
~~~python
import random

# gera números aleatórios entre 0 e 5
guess = random.randint(0, 5)
input("Me faça uma pergunta: ")

if guess == 0:
   print("Sim, com certeza")
elif guess == 1:
   print("Parece bom")
elif guess == 2:
   print("Melhor não te dizer agora")
elif guess == 3:
   print("Não posso prever agora")
elif guess == 4:
   print("Não conte com isso")
elif guess == 5:
   print("Minhas fontes dizem não")
~~~
Para criar esse projeto precisamos gerar resultados aleatórios. 
Para isso, usamos o módulo **random** para gerar números aleatórios, com o comando **import random**.
Assim, usamos a função **randint**, que gera números inteiros aleatórios inteiros no intervalo especificado

### Loops

* **While loop**

O **while** loop é muito semelhante à estrutura do **if**, com a diferença que enquanto a condição booleana for verdadeira
o bloco interno continua sendo executado. Exemplo:
~~~python
>>> x = 0
>>> while x < 10:
        print(x)
        x = x + 1
0
1
2
...
9       
~~~
Iniciamos a variável __x__ com o valor de 0, e avaliamos se ela é menor que 10, como a condição é verdadeira o bloco interno é executado,
atualizamos o valor de **x** adicionando uma unidade com o **x = x + 1**. Ao final do loop, retornamos ao **while** para conferir a expressão, enquanto ela for verdadeira o *loop* continua
* **Atribuição aumentada**

Poderíamos ter escrito x += 1, em vez de x = x + 1. Este recurso é chamado de atribuição aumentada.

* **Loop infinito e break**

No exemplo anterior, se esquecermos de digitar **x = x + 1**, entraríamos por acidente em um loop infinito, porquanto a condição
**x < 10** seria sempre verdadeira. Porém , muitas vezes queremos um loop infinito, e para sairmos dele em algum momento, utilizamos
a instrução **break**, a qual pode ser usada sempre que quisermos interromper um *loop*:
~~~python
while = True
    resposta = input("Qual a capital do Canadá?")
    if resposta == "Ottawa"
        print("Acertou!")
        break
    else:
        print("Tente novamente")
~~~

* **Continue**

O **continue** é utilizado para voltar ao início do loop, mesmo antes de chegar a última linha dele. O **continue** força a volta para o 
início do loop
~~~python
while True:
    username = input("username?")
    if username != "neo":
        print("Nunca nem vi")
        continue
    senha = input("Qual a sua senha?")
    if senha == "1234":
        print("Bem-vindo, {}".format(username))
        print("Aceita um café")
        break
~~~
Observe que é o __continue__ que volta ao início do loop enquanto não é digitado o usuário correto

Nesse código utilizamos a {} na string do **print**, para demarcar em qual lugar entra o valor da variável __username__

* **Listas**

Com as listas pode-se armazenar uma coleção de dados. Para criar uma lista utiliza-se colchetes e separa-se os itens com vírgula. Cada item 
é associado a um índice, a contagem deles começa pelo número 0 e por meio desses índices, podemos acessar os itens
~~~python
>>> planetas = ["Marte", "Vênus", "Urano"]
>>> planetas[0]
"Marte"
>>> planetas[1]
"Vênus"
>>> planetas[2] = "Terra"
>>> planetas
["Marte", "Vênus", "Terra"]
~~~
Note que podemos substituir os valores existentes, como substituímos o valor de "Urano" para o valor "Terra"

* **For loops e Range**

O **for** é a estrutura de repetição mais popular do Python. Ela é muito conveniente para percorrer os objetos iteráveis, como as listas.
Por padrão, a contagem se inicia do 0 e vai percorrendo os valores:
~~~python
>>> for i in range(6):
     print(i)
0
1
2
3
4
5
~~~
O objeto **range** retorna uma sequência, na qual os valores são produzidos sob demanda, tornando-se mais eficiente, não sendo mais necessário 
produzir toda a lista em memória. O **range** ainda aceita a definição de um valor inicial, um valor final e um valor passo. Por exemplo, para imprimir
os números ímpares de 1 a 14, temos:
~~~python
>>> for x in range(1, 15, 2):
    print(x)
1
3
5
7
9
11
13 
~~~
PS: O valor de passo 2, faz um pulo de uma casa;

* **Enumerate**

Utilizado para saber o índice de cada elemento.
~~~sql
>>> for i ,planeta in enunerate(planetas)
        print(i, planeta)
0 Mercúrio
1 Vênus
2 Terra
...
~~~

* **Iteração de mais de uma lista**

Há situações em que queremos percorrer duas listas simultaneamente. Com o __zip__ isso é possível, ele nos permite desempacotar as listas simultaneamente
~~~python
>>> musicas = ["Another brick in the wall", "Stairway to heaven", "We will rock you", "My generation"]
>>> horarios = ["19:00", "19:45", "20:10", "20:30"]
>>> for m , h in zip(musicas, horarios):
        print(m,h)
Another brick in the wall 19:00
Stairway to heaven 19:45
We will rock you 20:10
My generation 20:30
~~~

* **Dicionários e for loops**

Os dicionários são uma coleção associativa, ou mapeada. Essa associação conecta uma chave a um valor.
~~~sql
>>> meu_dicio = {"nome": "Matheus", "idade": 22 }
>>> meu_dicio
{"nome": "Matheus", "idade": 22 }
>>> meu_dicio["nome"]
'Matheus'
>>> meu_dicio["idade"]
22
~~~
Podemos também iterar dicionários:
~~~sql
>>> skills = {"speed": 8, "strenght": 99}
>>> for k in skills:
        print(k)
speed
strenght
~~~
Podemos utilizar o método __items__ para percorrer juntamente com os valores:
~~~sql
>>> for k, v in skills.items():
        print(k, v)
speed 8
strenght 99
~~~
* **Else**

Os _loops_ têm a opção da cláusula **else**, que só é executada se o loop executar sem interrupções
~~~sql
frutas = ['pera', 'uva', 'maçã']
for fruta un frutas:
    if fruta == 'abacaxi':
        print("Encontrado")
        break
else:
    print("não encontrada")
~~~
