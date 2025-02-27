---
tags:
  - MATH/PROBABILITY
class: ITESO/PROB_STATISTICTS
source:
  - https://www.youtube.com/watch?v=yta8aiOTr5Y
author:
  - "@ME"
ZTTLKSTEN:
  - Literature/ownwritten
date: 2025-02-26
type:
  - exercises
  - Research
title: Combinaciones, permutaciones y principio multiplicativo
summary: formulas y definiciones de probabilidad
description: ""
toc: true
readTime: true
autonumber: true
math: true
showTags: false
hideBackToTop: false
---



# Regla de la multiplicación

También conocido como principio multiplicativo se aplica cuando tenemos dos instancias de *experimentos o eventos*. **Completamente independientes** y queremos calcular el número de posibles *out comes* o resultados posibles.


> [! Tip] # $\Im$ def
> #MATH/DEF
>Si un evento $A$ puede ocurrir de $n$ formas diferentes y un evento $B$ de $m$ formas diferentes, entonces ambos pueden ocurrir de $mn$ formas diferentes   



como curiosidad el número de formas en las que pueden ocurrir $A$ y $B$ coincide con el cardinal del producto cruz entre estos dos

$$\#(A\times B)$$



Con el principio multiplicativo se contabilizan las formas en las que pueden ocurrir $A$ y $B$, en las que se asume que el orden es irrelevante y los eventos son independientes.


# Permutaciones




Por otro lado, cuando tenemos una cadena de eventos **siempre**, en las que el **orden es importante** y queremos *contar* el número de veces en las que podrían ocurrir, entonces estaríamos buscando *el número de permutaciones* de estos eventos.

## $i.e.$

Se tiene $a,b,c$ que son eventos *seguros* (que ocurren siempre) en los que el orden en los que ocurren los mismos es relevante, y queremos saber todos los posibles *"ordenes"* o *formas* en las que pueden ocurrir.

Podemos expresar un orden o una forma con una cadena de la siguiente forma

$$abc$$


Ahora encontremos todas las permutaciones posibles.


$$1. ~~abc$$
$$2.~~acb$$
$$3.~~bac$$
$$4.~~bca$$
$$5.~~cab$$
$$6.~~cba$$


Se tienen 6 posibilidades. 

Cuando hablamos de *permutaciones de los eventos* es importante recordar que se pueden sustituir las variables que representan los eventos con casi cualquier cosa, pudiendo así sustituir para encontrar por ejemplo las posibles sub secuencias de caracteres, filas posibles con 4 personas, etc.




Si se desea encontrar el número de permutaciones no es necesario encontrar todos los órdenes de manera manual. Esto se puede realizar de manera abstracta con las fórmulas de permutaciones



### tomando todos los elementos (Permutaciones)


si se tienen $n$ objetos entonces existen $n!$ permutaciones posibles, donde $n!$ se define de la siguiente forma


$$n!:=n(n-1)(n-2)\dots (2)(1)$$

y ademas $$0! = 1$$.

Esto último puede resultar un poco extraño pero mas delante tomara sentido

### Tomando menos de en elementos


Existen muchos casos en los que en el conteo no se pueden tomar todos los elementos disponibles, por ejemplo, todos los posibles podios de una carrera de 20 corredores.

Para este conteo, es evidente que el orden importa, pero solo estamos nos importan el orden de 3 de los 20 corredores.


Para resolver este problema y encontrar el número de permutaciones (posibles podios de la carrera) podemos hacer uso de la siguiente fórmula


$$_{n}P_{r} = \frac{n!}{(n-r)!}$$

de donde $n$ es el número de *elementos* posibles y $r$ el número de elementos que se toman

### Permutaciones con remplazo 
Existe otro caso en el que se pueden repetir loeventots, como por ejemplo tirar un dado 3 veces.

A diferencia de los otros casos dondusábamosos un elemento y npodíamosos repetiraquíui al tirar de nuevo los dados puede salir el mismnúmerormásas de una vez.


En caso de estar frente a uno de estos casos, el numero de permutaciones es dado por 

$$n^k$$

de donde n son los elementos disponibles y $k$ el numero de repeticiones


# Combinaciones



Existen muchos otros problemas donde el orden no es importante, como por ejemplo el 11 inicial con el que sale a jugar un equipo con una plantilla de 25 jugadores.

Aunque pueda sonar similar, son cosas fundamentalmente diferentes y el número total de combinaciones y permutaciones es algo que se calcula también de forma diferente.


El número de las combinaciones de $n$ elementos posibles tomando $r$ se calcula de la siguiente forma 


$$\begin{pmatrix}
n \\
r
\end{pmatrix} = \frac{n!}{(n-r!)r!}$$.

Nótese que cuando $n=r$ las combinaciones son igual a 1, esto tiene sentido, ya que si nuestro supuesto equipo tiene una plantilla de 11 jugadores solo existe un único equipo titular. 