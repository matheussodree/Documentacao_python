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
~~~pyhton
>>> largura = 10

>>> largura * 2
20
~~~

  Uma vez criada uma variável, podemos substituir o valor que ela contém
    
~~~pyhton
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


  
