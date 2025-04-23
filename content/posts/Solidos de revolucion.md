---
tags:
  - MATH/CALCULUS/INTEGRAL
class: ITESO/CALCULO_INTEGRAL
source:
  - leithold book
author:
  - "@ME"
ZTTLKSTEN:
  - Literature/ownwritten
date: 2025-04-20
type:
  - Project
title: Solidos de revolucion
summary: Documentacion del proyecto de solidos de
description: "Equipo: Juan Pablo Arroyo, Aaron Becerra, Fernando Santoyo"
toc: true
readTime: true
autonumber: true
math: true
showTags: false
hideBackToTop: false
---




# Objetivo del proyecto

El objetivo final de este proyecto es poder estimar el volumen de una botella de coca cola de 355 ml retornable solamente tomando del diámetro de la misma




# 1. El volumen

# 1.1 Como se calcula el volumen

Antes de empezar a calcular volúmenes de sólidos de revolución es pertinente reflexionar un poco sobre como calculamos el volumen en primer lugar, y que es lo que volumen significa.

## 1.2 Volumen


### 1.2.1 El desarrollo de la noción de volumen  

El volumen surge antes de todo desarrollo matemático como una magnitud de interés no solo en la física elemental, sino también para casi toda actividad humana. En todo momento interactuamos con objetos en nuestro espacio, que tienen **volumen**, tienen un contorno y un interior que no puede ser ocupado por ninguna otra cosa. El interés en la formulación de métodos para calcular esta magnitud es de evidente importancia para ramas como la ingeniería, la física, la Arquitectura o incluso la logística. No obstante en la antigüedad este desarrollo siempre se vería opacado por el desarrollo de la matemática de la geometría bidimensional y el cálculo de *Áreas* por parte de los griegos, que para sorpresa de nadie se trata del *volumen* (**medida**) en un espacio de una dimensión menor.

Una excepción más que destacable de esta tendencia y fascinación griega por las figuras planas es Arquímedes. Que se destacó por sus descubrimientos de las relaciones entre volúmenes de diferentes cuerpos, como mejor ejemplo el descubrimiento de que *el volumen de la esfera es  $\frac{2}{3}$ la del cilindro en el que está inscrito.* Este descubrimiento le fascinaba tanto a Arquímedes que se tallaría en su tumba a su petición. Todos estos descubrimientos fueron hechos a través de su famoso método de exacción que en su formulación yace la idea esencial del cálculo integral y los infinitesimales. 


Otro importante avance en la caracterización rigurosa de la noción de volumen fue dada por *Buenaventura Cavalieri*, que bajo su principio establecio que 

No obstante las matemáticas no acatarían la noción de volumen hasta la formulación de la **teoría de la medida**. Esta teoría generaliza la noción de volumen para espacios y conjuntos en dimensiones superiores. La naturaleza de esta teoría es más del interés del análisis y la topología que de la de la geometría, no obstante resulta útil para la comprensión de nuestro cometido, pues enlaza de manera general la noción de integral con la de *volumen* o *medida*.

> "La noción de medida es una generalización de las ideas de longitud, área o volumen. Como veremos, toda medida lleva además aparejada una correspondiente noción de Integral. "
> - *José C. Sabina de Lis*  


Para entender como es que se calcula el volumen de cuerpos tridimensionales con herramientas de cálculo de una variable es importante también entender la aparente de la situación 



# 2 Obteniendo el volumen de la botella

## 2.1 Tomando puntos de muestreo de la botella

Este paso consiste en obtener la materia prima con la que estaremos trabajando, apartir los resultados siguientes del proyecto se derivan de estos datos.

Estos datos toman la forma de dos sucesiónes  $x_{0},x_{1},\dots,x_{n}$ y $y_{0},y_{1},\dots,y_{n}$  de donde $x_{i}$ es el largo de la botella apartir del cuello y   $y_{i}$ es el radio de la botella en $x_{i}$


### 2.1.1 Procedimiento

Se desean obtener los puntos apartir de una botella de coca cola retornable de 355ml

!![Image Description](https://matutedevelop.github.io/blogg/images/Pasted%20image%2020250420133506.png)



La idea es sencilla, por la forma en la que se calcula el volumen del sólido de revolución con el método de discos necesitamos que nuestro integrando sea una función que nos devuelva el radio de la botella a lo largo de longitud de la botella. 





![[Solidos de revolucion 2025-04-20 13.22.51.excalidraw]]

Entonces con ayuda de un bernier y una cinta metrica medimos el *diametro* de la botella a lo largo de 24 puntos equidistantes por 1cm, y atraves de la relacion del radio de la circunferencia con s diametro se obtuvo cada punto $y_{i}$

$$
r=y_{i}=\frac{d}{2}
$$

Se obtuvieron los siguientes datos.

|   i  |   0 |   1 |    2 |    3 |    4 |    5 |    6 |    7 |    8 |    9 |   10 |   11 |   12 |   13 |   14 |   15 |   16 |   17 |   18 |   19 |   20 |   21 |   22 |   23 |   24 |
|:----|----:|----:|-----:|-----:|-----:|-----:|-----:|-----:|-----:|-----:|-----:|-----:|-----:|-----:|-----:|-----:|-----:|-----:|-----:|-----:|-----:|-----:|-----:|-----:|-----:|
| yᵢ  | 1.4 | 1.3 | 1.25 | 1.35 | 1.45 | 1.65 | 1.95 | 2.35 | 2.55 | 2.75 | 2.89 |  3.0 | 3.05 |  3.1 | 3.13 | 3.05 | 2.9  | 2.8  | 2.7  | 2.6  | 2.55 | 2.7  | 3.05 | 3.15 | 2.85 |
| xᵢ  | 0   | 1   | 2    | 3    | 4    | 5    | 6    | 7    | 8    | 9    | 10   |  11  | 12   | 13   | 14   | 15   | 16   | 17   | 18   | 19   | 20   | 21   | 22   | 23   | 24.5 |





Graficando se confirma efectivamente  asemejan la silueta de la botella partida a la mitad.

![[Pasted image 20250420131758.png|1000]]


## 2.2 Ajustando curva a los puntos

El siguiente paso es poder encontrar una curva que se asemeje a la de la botella. Debido a que se cuenta con una cantidad relativamente generosa de puntos, el primer método que intentamos es el de interpolación.

### 2.2.1Interpolación

Interpolar quiere decir que para nuestros puntos $(x_{0},y_{0}),(x_{1},y_{1}),\dots(x_{n},y_{n})$ buscamos encontrar una función $f$ tal que $f(x_{i}) = y_{i}$. Debido a las bondades de los polinomios, en especial a la hora de la integración, buscamos que nuestra función interpoladora sea un polinomio.

#### 2.2.1.2 Teorema de aproximación de Weirstrass

Si en lugar de contar con un número finito de puntos tuviéramos la curva exacta de la silueta de la coca-cola podría parecer que todo sería más sencillo, integraríamos dicha función y listo no es así? En realidad no es tan sencillo, si tuviéramos la función exacta de la silueta de la botella lo más probable es de que su expresión sería absurdamente complicada o de lleno no podría ser escrita como una composición de funciones *básicas* como son las funciones polinómicas, radicales, racionales o las trascendentales, es decir estaríamos ante una función no elemental.

No obstante eso no es limitante para encontrar una función *sencilla* que nos sea útil y que se parezca mucho

#####  $\S ~2.1~~\mathbb{T}\mathrm{eorema~de~aproximación ~ de} \mathcal{~Weirstrass}$


sea $f:[a,b] \to \mathbb{R}$ una función continua, entonces existe una sucesión de polinomios $P_{n}$ tal que $P_{n}$ *converge uniformemente* a $f$, o dicho de otra forma 

$$\forall f \in C[a,b]~~ \exists(P_{n}):$$
$$\lim P_{n} \to f $$

Una consecuencia directa de este teorema es la de que nos podemos acercar a cualquier función continua en un intervalo cerrado de forma arbitraria. Gracias a este teorema sabemos que sin importar que tan pronunciada o complicada pueda ser la curva de una función continua, podemos aproximarnos a dicha función cuanto queramos con un polinomio. Esto es porque los polinomios son densos en el espacio $C[a,b]$.


#### Polinomios interpoladores del grado minimo

Los dos métodos más sencillos de entender para construir un polinomio son los polinomios de Lagrange o plantear una matriz de *Vandermonde*

Estos dos procedimientos son equivalentes, y de forma simbólica producen el mismo resultado. Un polinomio $P_{n}$ (*con grado menor o igual a $n$*).

Esto es una consecuencia del siguiente teorema

##### $\S~2.2~~\mathbb{T}\mathrm{eorema}$

dada la sucesion de puntos $(x_{0},y_{0}),(x_{1},y_{1}),\dots,(x_{n,y_{n}})$ con $x_{0}<x_{1}<\dots<x_{n}$
existe un único polinomio $P_{n}$ de grado menor o igual a $n$ tal que $P_{n}(x_{i})=y_{i}$, $i=0,1,\dots,n$ 

$$
\exists!P \in \mathbb{R}^n[x]:P(x_{i}) = y_{i}, i=0,1,\dots,n
$$

###### Demostración

si $P$ existe entonces se tiene que
$$P(x_{0})=a_{0}+a_{1}x_{0}+a_{2}x_{0}^2+\dots+a_{n}x_{0}^{n} = y_{0}$$
$$P(x_{1})=a_{0}+a_{1}x_{1}+a_{2}x_{1}^2+\dots+a_{n}x_{1}^{n} = y_{1}$$
$$\vdots$$
$$P(x_{n})=a_{0}+a_{1}x_{n}+a_{2}x_{n}^2+\dots+a_{n}x_{n}^{n} = y_{n}$$

de dode se tiene la matriz caracteristica

$$A=
\begin{bmatrix}
1&x_{0}&x_{0}^2&\dots&x_{0}^n \\
1&x_{1}&x_{1}^2&\dots&x_{1}^n \\
\vdots&\vdots&\vdots&\ddots& \vdots\\
 1&x_{n}&x_{n}^2&\dots&x_{n}^n 
\end{bmatrix}
$$

y el vector de resultados 

$$b=
\begin{bmatrix}
y_{0} \\
y_{1} \\
\vdots \\
y_{n}
\end{bmatrix}
$$

entonces de nuestro sistema de ecuaciones inicial tenemos 


$$AX=b$$
$$
\begin{bmatrix}
1&x_{0}&x_{0}^2&\dots&x_{0}^n \\
1&x_{1}&x_{1}^2&\dots&x_{1}^n \\
\vdots&\vdots&\vdots&\ddots& \vdots\\
 1&x_{n}&x_{n}^2&\dots&x_{n}^n 
\end{bmatrix}

\begin{bmatrix}
a_{0} \\
a_{1} \\
\vdots \\
a_{n}
\end{bmatrix}

=

\begin{bmatrix}
y_{0} \\
y_{1} \\
\vdots \\
y_{n}
\end{bmatrix}
$$


En orden para que el postulado del teorema se cumpla se necesita que el sistema tenga una única solución, es decir $\det(A)\neq 0$.

Supongamos que $\det(A)=0$ esto implica que las columnas de la matriz $A$ no son *linealmente independientes*. Esto se puede expresar de la siguiente manera.

sea

$$
C_{i}=\begin{bmatrix}
x_{0}^i &
x_{1}^i &
\dots &
x_{n}^i

\end{bmatrix}^{\intercal}
$$

$$C_{i} \in \mathscr{L}(C_{j}),~~~~~~j\neq i$$


donde $\mathscr{L}(u_{0},u_{1},\dots)$ es el *espacio de combinaciones lineales* de los vectores $u_{1},u_{2},\dots$

---
los vectores $C_{1},C_{2},\dots,C_{n}$ sean linealmente independientes implica que $\det(A)\neq 0$ que a su vez implica el postulado del teorema 2.2

se desea demostrar por inducción que 
$$C_{r} \notin \mathscr{L}(C_{s})~~~~ 0 \leq s < r \leq n$$

**Caso base**

$$C_{1} \notin \mathscr{L}(C_{0})$$


desde que $x_{0}<x_{1}<\dots x_{n}$
$$
\begin{bmatrix}
x_{0} \\
x_{1} \\
\vdots \\
x_{n}
\end{bmatrix}

\neq

k
\begin{bmatrix}
1 \\
1 \\
\vdots \\
1
\end{bmatrix}
~~~~ k\in \mathbb{R}
$$

**Paso inductivo**

se asume 

$$C_{r} \in \mathscr{L}(C_{s})~~~~ 0 \leq s < r \leq n$$


$$
b_{0}C_{0}+b_{1}C_{1}+\dots+b_{r-1}C_{r-1} = C_{r}

$$

$$

\begin{bmatrix}
b_{0} \\
b_{0} \\
\vdots \\
b_{0}
\end{bmatrix}
+
\begin{bmatrix}
b_{1}x_{0} \\
b_{1}x_{1} \\
\vdots \\
b_{1}x_{n}
\end{bmatrix}
+ \dots +
\begin{bmatrix}
b_{r-1}x_{n}^{r-1} \\
b_{r-1}x_{n}^{r-1} \\
\vdots \\
b_{r-1}x_{n}^{r-1}
\end{bmatrix}

=

\begin{bmatrix}
x_{0}^r \\
x_{1}^r \\
\vdots \\
x_{n}^r
\end{bmatrix}

$$

$$

\begin{bmatrix}
b_{0} \\
b_{0} \\
\vdots \\
b_{0}
\end{bmatrix}
+
\begin{bmatrix}
b_{1}x_{0} \\
b_{1}x_{1} \\
\vdots \\
b_{1}x_{n}
\end{bmatrix}
+ \dots +
\begin{bmatrix}
b_{r-1}x_{n}^{r-1} \\
b_{r-1}x_{n}^{r-1} \\
\vdots \\
b_{r-1}x_{n}^{r-1}
\end{bmatrix}
-
\begin{bmatrix}
x_{0}^r \\
x_{1}^r \\
\vdots \\
x_{n}^r
\end{bmatrix}
=

\begin{bmatrix}
0 \\
0 \\
\vdots \\
0
\end{bmatrix}

$$

Igualando las sumas de los componentes se obtiene un polinomio $Q$ de la forma:

$$

Q(x_{0})=b_{0}+b_{1}x_{0}+b_{2}x_{0}^2+\dots+b_{r-1}x_{0}^{r-1}-x_{0}^r=0
$$

$$

Q(x_{1})=b_{0}+b_{1}x_{1}+b_{2}x_{1}^2+\dots+b_{r-1}x_{1}^{r-1}-x_{1}^r = 0
$$

$$\vdots$$

$$
Q(x_{n})=b_{0}+b_{1}x_{n}+b_{2}x_{n}^2+\dots+b_{r-1}x_{n}^{r-1}-x_{n}^r = 0
$$


Por el *Teorema fundamental del álgebra* un polinomio de grado $m$ tiene a lo sumo $m$ raíces.


En el mejor de los casos $r=n$, no obstante el polinomio $Q$ tiene $n+1$ raíces, lo que es una contradicción con el Teorema fundamental del algebra, por lo tanto 


$$C_{r}\notin \mathscr{L}(C_{s})~~~~0\leq s<r\leq n$$

# Porque Lagrange vs MLS


- Lagrange se centra en interpolar en los puntos dados, es decir $P(x_{i})=y_{i}$, prioriza eso  y le vale madre el error






# Bibliografia

- https://static.sumaysigue.uchile.cl/disponibilizacion_aula360/G3D/U3%20-%20Generaci%C3%B3n%20de%20cuerpos%20utilizando%20patrones%20geom%C3%A9tricos/T2%20-%20Volumen%20de%20cuerpos%20geom%C3%A9tricos_/C1%20-%20Volumen%20y%20Principio%20de%20Cavalieri/Apunte%20Volumen%20y%20Principio%20de%20Cavalieri.pdf
- Curso_Teoria_Medida.pdf
- file:///C:/Users/fofoy/Downloads/ENTRETEXTOS-30-L2.pdf

