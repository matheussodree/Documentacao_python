# Documentacao_python
Documentação dos estudos de python (extraídos do livro "Python direto ao ponto" do Estevão Fonseca)

### Conceitos importantes:

* Programa:
  Um programa é uma sequência de instruções para executar operações de computação.

* Algoritmo:
  As sequências de instruções que criamos com fim de solucionar problemas são chamadas de algoritmo

### Início:
* Hello world

~~~python

print("Hello world")

~~~


* Valores Inteiros, tipo _Int_

~~~python
>>> 2
2
~~~

* Valores flutuantes, tipo _float_
~~~python
>>> 1.61
1.61
~~~

* Valores tipo _String_
~~~python
>>> "Hello world"
Hello world
>>> 'Hello world'
Hello world
~~~

* Valores Booleanos
~~~python
>>> True
True
>>> False
False
~~~

* Variáveis

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

* Nome das variáveis

  Válido | Inválido | Por quê é inválido?
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

* Operadores Aritméticos

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

* Operações com Strings

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

* Comentários

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

""" Cálculo da área de um retângulo"""
base = 2
largura = 3
print("área do retângulo "+str(base*largura))

área do círculo 50.24
área do retângulo 6
~~~
