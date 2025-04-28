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

El objetivo final de este proyecto es poder estimar el volumen de una botella de coca cola de 355 ml retornable solamente tomando muestras  del diámetro de la misma






# 1.1 Como se calcula el volumen

Antes de empezar a calcular volúmenes de sólidos de revolución es pertinente reflexionar un poco sobre como calculamos el volumen en primer lugar, y que es lo que volumen significa.

## 1.2 Volumen


### 1.2.1 El desarrollo de la noción de volumen  

El volumen surge antes de todo desarrollo matemático como una magnitud de interés no solo en la física elemental, sino también para casi toda actividad humana. En todo momento interactuamos con objetos en nuestro espacio, que tienen **volumen**, tienen un contorno y un interior que no puede ser ocupado por ninguna otra cosa. El interés en la formulación de métodos para calcular esta magnitud es de evidente importancia para ramas como la ingeniería, la física, la Arquitectura o incluso la logística. No obstante en la antigüedad este desarrollo siempre se vería opacado por el desarrollo de la matemática de la geometría bidimensional y el cálculo de *Áreas* por parte de los griegos, que para sorpresa de nadie se trata del *volumen* (**medida**) en un espacio de una dimensión menor.

Una excepción más que destacable de esta tendencia y fascinación griega por las figuras planas es Arquímedes. Que se destacó por sus descubrimientos de las relaciones entre volúmenes de diferentes cuerpos, como mejor ejemplo el descubrimiento de que *el volumen de la esfera es  $\frac{2}{3}$ la del cilindro en el que está inscrito.* Este descubrimiento le fascinaba tanto a Arquímedes que se tallaría en su tumba a su petición. Todos estos descubrimientos fueron hechos a través de su famoso método de exacción que en su formulación yace la idea esencial del cálculo integral y los infinitesimales. 


Otro importante avance en la caracterización rigurosa de la noción de volumen fue dada por *Buenaventura Cavalieri*, que bajo su principio estableció que 

No obstante las matemáticas no acatarían la noción de volumen hasta la formulación de la **teoría de la medida**. Esta teoría generaliza la noción de volumen para espacios y conjuntos en dimensiones superiores. La naturaleza de esta teoría es más del interés del análisis y la topología que de la de la geometría, no obstante resulta útil para la comprensión de nuestro cometido, pues enlaza de manera general la noción de integral con la de *volumen* o *medida*.

> "La noción de medida es una generalización de las ideas de longitud, área o volumen. Como veremos, toda medida lleva además aparejada una correspondiente noción de Integral."
> - *José C. Sabina de Lis*  


Para entender como es que se calcula el volumen de cuerpos tridimensionales con herramientas de cálculo de una variable es importante también entender la aparente de la situación 



# 2 Obteniendo el volumen de la botella

## 2.1 Tomando puntos de muestreo de la botella

Este paso consiste en obtener la materia prima con la que estaremos trabajando, a partir los resultados siguientes del proyecto se derivan de estos datos.

Estos datos toman la forma de dos sucesiones  $x_{0},x_{1},\dots,x_{n}$ y $y_{0},y_{1},\dots,y_{n}$ de donde $x_{i}$ es el largo de la botella a partir del cuello y   $y_{i}$ es el radio de la botella en $x_{i}$

Apartir de aqui a los puntos $(x_{i},y_{i})$ se les denominara *nodos*


### 2.1.1 Procedimiento

Se desean obtener los nodos a partir de una botella de coca cola retornable de 355 ml

!![Image Description](https://matutedevelop.github.io/blogg/images/Pasted%20image%2020250420133506.png)



La idea es sencilla, por la forma en la que se calcula el volumen del sólido de revolución con el método de discos necesitamos que nuestro integrando sea una función que nos devuelva el radio de la botella a lo largo de longitud de la botella. 





![[Solidos de revolucion 2025-04-20 13.22.51.excalidraw]]

Entonces con ayuda de un bernier y una cinta métrica medimos el *diámetro* de la botella a lo largo de 24 nodos equidistantes por 1 cm, y a través de la relación del radio de la circunferencia con su diámetro se obtuvo cada punto $y_{i}$

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


## 2.2 Ajustando curva a los nodos

El siguiente paso es poder encontrar una curva que se asemeje a la de la botella. Debido a que se cuenta con una cantidad relativamente generosa de nodos, el primer método que intentamos es el de interpolación.


#### 2.2.1 Teorema de aproximación de Weirstrass

Si en lugar de contar con un número finito de nodos tuviéramos la curva exacta de la silueta de la coca-cola podría parecer que todo sería más sencillo, integraríamos dicha función y listo no es así? En realidad no es tan sencillo, si tuviéramos la función exacta de la silueta de la botella lo más probable es de que su expresión sería absurdamente complicada o de lleno no podría ser escrita como una composición de funciones *básicas* como son las funciones polinómicas, radicales, racionales o las trascendentales, es decir estaríamos ante una función no elemental.

No obstante eso no es limitante para encontrar una función *sencilla* que nos sea útil y que se parezca mucho

#####  $\S \space2.1\space\space\mathbb{T}\mathrm{eorema\space de\space aproximación \space de} \mathcal{~Weirstrass}$


sea $f:[a,b] \to \mathbb{R}$ una función continua, entonces existe una sucesión de polinomios $P_{n}$ tal que $P_{n}$ *converge uniformemente* a $f$ , o dicho de otra forma 

$$\forall f \in C[a,b]~~ \exists (P_{n}):$$
$$\lim P_{n} \to f $$

Una consecuencia directa de este teorema es la de que nos podemos acercar a cualquier función continua en un intervalo cerrado de forma arbitraria. Gracias a este teorema sabemos que sin importar que tan pronunciada o complicada pueda ser la curva de una función continua, podemos aproximarnos a dicha función cuanto queramos con un polinomio. Esto es porque los polinomios son densos en el espacio $C[a,b]$.


###  2.2.2 Interpolación (*Opcion 1*)

Interpolar quiere decir que para nuestros nodos $(x_{0},y_{0}),(x_{1},y_{1}),\dots(x_{n},y_{n})$ buscamos encontrar una función $f$ tal que $f(x_{i}) = y_{i}$. Debido a las bondades de los polinomios, en especial a la hora de la integración, buscamos que nuestra función interpoladora sea un polinomio.




#### 2.2.2.2 Polinomios interpoladores del grado mínimo

Los dos métodos más sencillos de entender para construir un polinomio son los polinomios de Lagrange o plantear una matriz de *Vandermonde*

Estos dos procedimientos son equivalentes, y de forma simbólica producen el mismo resultado. Un polinomio $P_{n}$ (*con grado menor o igual a $n$*).

Esto es una consecuencia del siguiente teorema

##### $\S~2.2~~\mathbb{T}\mathrm{eorema}$

dada la sucesion de nodos $(x_{0},y_{0}),(x_{1},y_{1}),\dots,(x_{n,y_{n}})$ con $x_{0}<x_{1}<\dots<x_{n}$
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

de donde se tiene la matriz característica

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

Sea

$$
C_{i}=\begin{bmatrix}
x_{0}^i &
x_{1}^i &
\dots &
x_{n}^i

\end{bmatrix}^{\intercal}
$$

$$C_{i} \in \text{span}(C_{j_{0}},C_{j_{2}},\dots,C_{j_{n}}),~~~~~~j_{i}\neq i$$


donde $\text{span}(u_{0},u_{1},\dots)$ edos *espacio de combinaciones lineales* de los vectores $u_{1},u_{2},\dots$

---

Para demostrar que los vectores $C_{1},C_{2},\dots,C_{n}$ sean linealmente independientes basta con demostrar que $C_{r}\notin \text{span}(C_{r-1},\dots ,C_{0})$ implica que $\det(A)\neq 0$ que a su vez implica el postulado del teorema 2.2

se desea entonces demostrar  que 
$$C_{r} \notin \text{span}(C_{r-1},C_{r-2},\dots C_{0})~~~~ 0 < r \leq n$$



supongamos que 

$$C_{r} \in \text{span}(C_{r-1},C_{r-2},\dots,C_{0} )~~~~ 0  < r \leq n$$

entonces $\exists b=(b_{0},b_{1},\dots,b_{r-1})$ tal que 

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
b_{r-1}x_{0}^{r-1} \\
b_{r-1}x_{1}^{r-1} \\
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
b_{r-1}x_{0}^{r-1} \\
b_{r-1}x_{1}^{r-1} \\
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

Igualando las sumas de los componentes se obtiene un polinomio $Q$ de grado $n$ que satisface que:

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


> Por el *Teorema fundamental del álgebra* un polinomio de grado $m$ tiene a lo sumo $m$ raíces.


En el mejor de los casos $r=n$, no obstante el polinomio $Q$ tiene $n+1$ raíces, lo que es una contradicción con el Teorema fundamental del álgebra, por lo tanto, 

$$C_{r}\in \text{span}(C_{r-1},C_{r-2},\dots,C_{0})~~~~0<r\leq n$$

es una contradicción con el teorema fundamental del álgebra y Con esto queda demostrado que 


$$C_{r}\notin \text{span}(C_{r-1},C_{r-2},\dots,C_{0})~~0<r\leq n$$


Y que toda la columna $C_{r}$ de la matriz $A$ por definición tienen que ser linealmente independiente a las columnas $C_{r-1},C_{r-2},\dots ,C_{0}$. Por lo tanto, $\det(A)\neq 0$ y el sistema $AX=b$ tiene solución única. Demostrando así el teorema 2.2


#### 2.2.2.3 Polinomios de Lagrange

se define 

$$
l_{n,i}(x) = \prod_{\substack{j=0\\ j\neq i} }^n \frac{x-x_{j}}{x_{i}-x_{j}} 
$$

un polinomio de grado $n+1$ con sus raíces en $x_{j}$ si $j\neq i$

$$
l_{n,i}(x_{j}) = \prod_{\substack{j=0\\ j\neq i} }^n \frac{x_{j}-x_{j}}{x_{i}-x_{j}} = 0 
$$


además 

$$
l_{n,i}(x_{i}) = \prod_{\substack{j=0\\ j\neq i} }^n \frac{x_{i}-x_{j}}{x_{i}-x_{j}} = 1 
$$

Definiendo 
$$L_{n}(x)= \sum_{i=0}^n y_{i}l_{n,i}(x)$$

$$L_{n}(x_{i})= y_{0}l_{n,0}(x_{i})+y_{1}l_{n,1}(x_{i})+\dots+y_{i}l_{n,i}(x_{i})+\dots+ y_{n}l_{n,n}(x_{i})$$

$$L_{n}(x_{i})=y_{i}$$ 
es el polinomio de grado menor o igual a $n$ que interpola en la sucesión de nodos $(x_{0},y_{0}),(x_{1},y_{1}),\dots(x_{n},y_{n})$

##### Procedimiento

para encontrar el polinomio de Lagrange dada por la sucesión de nodos, podemos utilizar el siguiente código 

```python
import scipy as sc

poly = sc.interpolate.lagrange(x_i,y_i)

```

que nos regresa una instancia de la clase `polynomial` que es nuestra función.Graficando el polinomio se tiene el siguiente ajuste.

!![Image Description](https://matutedevelop.github.io/blogg/images/Pasted%20image%2020250423125609.png)


El ajuste en general no es bueno, y partir de ciertos nodos el polinomio parece que ya no interpola los nodos correspondientes. La hipótesis es que coeficientes del polinomio no pueden ser obtenidos correctamente por el procedimiento previo debido a las limitaciones que tienen las computadoras con las operaciones de punto flotante. Lo que provoca que el polinomio devuelto por la función sea diferente al verdadero polinomio de Lagrange. 

Otra razón por la cual podríamos estar ocurriendo esto es por la elección de nodos y el número de nodos. Al tener 25 nodos de interpolación el polinomio resultante es de grado 25, lo que causa que pueda crecer o decrecer muy rápido en intervalos pequeños. En cuanto la elección de nodos si los nodos son equidistantes el efecto *runge* sé magnífica. 

###### Efecto runge 

El efecto runge es un fenómeno común cuando se hace aproximación por polinomios y nuestro polinomio tiene un grado elevado.  Lo que resulta en oscilaciones en los extremos del intervalo de interpolación.


Existen varias alternativas para poder obtener un mejor ajuste, el primero sería utilizar una cantidad menor de nodos. El segundo es que en lugar de tomar las muestras equidistantes, tomar  más muestras en los bordes del intervalo, esto ayuda a minimizar las oscilaciones. Un criterio Formal para la elección de estos puntos es usar los *nodos de chebyshev*, que son las raíces de *los polinomios de chebyshev de primera especie*. De forma más especifica para la eleccion de los nodos $(x_{0},y_{0}),(x_{1},y_{1}),\dots(x_{n},y_{n})$ elegimos para los valores de $x_{i}$ las raíces del polinomio $T_{n+1}$

Los polinomios de chebyshev de primera especie se definen de la siguiente manera:

$$
T_{n}(x)=\cos(n\arccos x),~~~ x\in[-1,1]
$$


Que con ayuda de identidades trigonométricas pueden ser definidos de manera recursiva. 

$$
T_{n+1}(x)=2xT_{n}(x)-T_{n-1}(x)
$$

y dado que $T_{0}(x)=0$ y $T_{1}(x)=x$ podemos llegar expresar $T_{n}$ como un polinomio.

> Nota:
> $\cos(n\arccos x)$es una función que está definida solamente en $[-1,1]$ y su imagen es $[-1,1]$ es decir que está restringida. No obstante, cuando $\cos(n\arccos x)$ se **expande** a $T_{n}(x)$ en su forma polinómica, esta restricción desaparece.  $\cos(n\arccos x)\neq T_{n}(x)$ son funciones con distintas con dominio e imagen diferentes con la peculiaridad de que mapean a los mismos valores en $[-1,1]$ 

### 2.2.3 Ajuste por mínimos cuadrados  **OLS** (opción 2)


Nuestro siguiente intento fue obtener nuestro polinomio a través del método de mínimos cuadrados. Este procedimiento es fundamentalmente diferente en cuestión de  cuáles y como son los elementos e hiperparámetros con el que el investigador puede experimentar y que evidentemente producen resultados fundamentalmente distintos al de los polinomios de Lagrange.

En el ajuste de polinomios por mínimos cuadrados se escoge primero el grado del polinomio que queremos que **aproxime** los nodos. Si elegimos un polinomio de grado $n$ tendremos $a_{0},a_{1},\dots,a_{m}$ coeficientes y al igual que en él procedimento anterior, nuestra tarea es encontrar la mejor elección de $a_{0},a_{1},\dots,a_{m}$.


$$\phi(a_{0},a_{1},\dots,a_{m},x)=a_{0}+a_{1}x+a_{2}x^2+\dots+a_{m}x^m=\sum_{i=0}^m a_{i}x^i$$

La $\phi$ nos permite explorar el espacio $\mathbb{R}^n[x]$  y comparar sus valores en $x_{i}$ y apartir de ahi ver si la funcion nos es de utilidad.



!![Image Description](https://matutedevelop.github.io/blogg/images/Pasted%20image%2020250426210948.png)
> La figura anterior ejemplifica  el espacio y sus elementos tienen diferentes *errores* respecto a los nodos

$$
\epsilon=\sum_{i=0}^n[y_{i}-\phi(a_{0},a_{1},\dots,a_{m},x_{i})]^2
$$

Se denomina *Error cuadrado*  y es una funcion dependiente de $a_{0},a_{1},\dots,a_{m}$. La mejor o las mejores elecciones de estos valores ocurre cuando se minimiza $\epsilon$. Es decir que estamos ante un problema de optimizacion.

#### Minimizar una funcion de varias variables 

!![Image Description](https://matutedevelop.github.io/blogg/images/Pasted%20image%2020250426212345.png)


los minimos locales de una funcion de varias variables $f$ se encuentran en aquellos puntos ta que el *gradiente de la funcion* es el vector nulo

$$\nabla f(x_{1},x_{2},\dots,x_{m})= \begin{bmatrix}
0 \\
0 \\
\vdots \\
0
\end{bmatrix}$$

$\nabla f$ es una *funcion vectorial* que devuelve un vector cuya direccion nos indica hacia donde movernos en el espacio $\mathbb{R}^n$ de tal forma que el valor de $f$ aumente lo mas posible en ese punto. Otra interpretacion es que el vector gradiente tiene la misma direccion a la del plano tangente  a $f$ en ese punto. Similar a la recta tangente al punto en una variable


![[Solidos de revolucion 2025-04-26 23.49.24.excalidraw|800]]



Es decir que el $\nabla f$ vale lo mismo 0 en los máximos y mínimos locales, además de en una clase de puntos denominados puntos silla. 
El vector gradiente se  define como

$$
\nabla f=\begin{bmatrix}
\frac{\partial f}{\partial x_{1}} \\
\frac{\partial f}{\partial x_{2}} \\
\vdots \\
\frac{\partial f}{\partial x_{m}}
\end{bmatrix}

$$

#### Minimizando $\epsilon$

Regresando a la función

$$
\epsilon=\sum_{i=0}^n[y_{i}-\phi(a_{0},a_{1},\dots,a_{m},x_{i})]^2
$$

Se tiene que cumplir que $\frac{\partial \epsilon}{\partial a_{l}}=0$ con  $l=0,1,\dots,m$

$$
\epsilon=\sum_{i=0}^n[y_{i}^2-2y_{i}\phi(a_{0},a_{1},\dots,a_{m},x_{i})+ \phi(a_{0},a_{1},\dots,a_{m},x_{i})^2]
$$

$$
\epsilon=[\sum_{i=0}^ny_{i}^2- \sum_{i=0}^n2y_{i}\phi(a_{0},a_{1},\dots,a_{m},x_{i})+ \sum_{i=0}^n\phi(a_{0},a_{1},\dots,a_{m},x_{i})^2]
$$

$$
\epsilon=[\sum_{i=0}^ny_{i}^2- \sum_{i=0}^n2y_{i}\sum_{j=0}^m a_{i}x^i+ \sum_{i=0}^n (\sum_{j=0}^m a_{j}x_{i}^j)^2]
$$


$$
\epsilon=[\sum_{i=0}^ny_{i}^2- \sum_{i=0}^n2y_{i}\sum_{j=0}^m a_{j}x_{i}^j+ \sum_{i=0}^n \sum_{j=0}^m a_{j}x_{i}^j \sum_{k=0}^m a_{k}x_{i}^k]
$$


buscamos encontrar la derivada repecto a las variables de las que depende $\epsilon$. vamos termino por termino

1. $\sum_{i=0}^ny_{i}^2$
no tiene $a_{l}$ por ninguna parte, por lo que es constante respecto a esta variable

$$\frac{\partial \epsilon}{\partial a_{l}}\sum_{i=0}^ny_{i}^2=0$$

2.  Para el segundo termino podemos hacer uso de los [*corchetes de iverson*](https://es.wikipedia.org/wiki/Corchete_de_Iverson) para simplificar un poco la notacion a fin de hacerlo un poco mas entendible.

$$\frac{\partial }{\partial a_{l}} - \sum_{i=0}^n2y_{i}\sum_{j=0}^m a_{j}x_{i}^j = \frac{\partial }{\partial a_{l}} -\sum_{i=0}^n\sum_{j=0}^m  2y_{i}a_{j}x_{i}^j~~[j=l]$$

los corchetes $[j=l]$ son una *propocision logica* que debe de ser verdadera en cada iteracion. Es decir. Sino se cumple la condicion no se suma nada. $j=l$ una sola vez durante todo el ciclo de $\sum_{j}$. Es decir que el resto de iteraciones  el termino es constante respecto a $a_{l}$. Por lo que se puede quitar la sumatoria y sustituir  $j$ por $l$


$$\frac{\partial }{\partial a_{l}} -2a_{l}\sum_{i=0}^n  y_{i}x_{i}^l=-2\sum_{i=0}^n  y_{i}x_{i}^l$$
3. 
$$\sum_{i=0}^n\sum_{j=0}^m a_{j}x_{i}^j \sum_{k=0}^m a_{k}x_{i}^k=\sum _{j=0}^m \sum _{k=0}^m a_{j}a_{k} \sum_{i=0}^n x_{i}^{j+k}$$

$$
\frac{\partial }{\partial a_{l}}\sum _{j=0}^m \sum _{k=0}^m a_{j}a_{k} \sum_{i=0}^n x_{i}^{j+k}= \sum _{j=0}^m \sum _{k=0}^m  [a_{k}[j=l] + a_{j}[k=l]] \sum_{i=0}^n x_{i}^{j+k} 
$$
al igual que en el caso anterior  cuando $j=l$ la sumatoria con indice $j$ se anula y queda solo $\sum_{k}^m a_{k}$, pasa exactamente lo mismo cuando $k=l$. Por lo tanto hay $m+1$ veces en las que solo queda $\sum a_{k}\sum \dots$ y $m+1$ veces en las que queda $\sum a_{j} \sum\dots$ pero estas dos son exactamente la misma suma por lo que tenemos al final

$$
2\sum_{k=0}^m a_{k}\sum _{i=0}^n x_{i}^{l+k}
$$


> alch esta parte esta confusa 


$$\frac{\partial \epsilon}{\partial a_{l}}=-2\sum_{i=0}^n  y_{i}x_{i}^l+2\sum_{k=0}^m a_{k}\sum _{i=0}^n x_{i}^{l+k}$$



-$2\sum_{i=0}^n  y_{i}x_{i}^l$ es un valor conocido por lo que lo podemos pasar al otro lado de la igualdad

$$\sum_{k=0}^m a_{k}\sum _{i=0}^n x_{i}^{l+k}=\sum_{i=0}^n  y_{i}x_{i}^l$$



Dando valores a $k,l$ se llega a un sistema de $m$ ecuaciones con $m$ variables 

$$ a_{0}\sum _{i=0}^n x_{i}^{0+0}+a_{1}\sum _{i=0}^n x_{i}^{1+0}+a_{2}\sum _{i=0}^n x_{i}^{2+0}+\dots+a_{n}\sum _{i=0}^n x_{i}^{n+0}=\sum_{i=0}^n  y_{i}x_{i}^0$$

$$ a_{0}\sum _{i=0}^n x_{i}^{0+1}+a_{1}\sum _{i=0}^n x_{i}^{1+1}+a_{2}\sum _{i=0}^n x_{i}^{2+1}+\dots+a_{n}\sum _{i=0}^n x_{i}^{n+1}  = \sum_{i=0}^n  y_{i}x_{i}^1$$


$$\vdots$$

$$ a_{0}\sum _{i=0}^n x_{i}^{0+n}+a_{1}\sum _{i=0}^n x_{i}^{1+n}+a_{2}\sum _{i=0}^n x_{i}^{2+n}+\dots+a_{n}\sum _{i=0}^n x_{i}^{n+n}  = \sum_{i=0}^n  y_{i}x_{i}^n$$


$$
\begin{bmatrix}
n&\sum_{i=0}^m x_{i}&\sum_{i=0}^mx_{i}^2\dots&\sum_{i=0}^n x_{i}^n\\
\sum_{i=0}^m x_{i} &\sum_{i=0}^m x_{i}^2 & \sum_{i=0}^m x_{i}^3\dots &\sum_{i=0}^m x_{i}^{n+1} \\ 
\vdots&\vdots&\vdots& \ddots&  \\
\sum_{i=0}^m x_{i}^n &\sum_{i=0}^m x_{i}^{n+1}&\sum_{i=0}^m x_{i}^{n+2}
&\dots \sum_{i=0}^m x_{i}^{2n}
\end{bmatrix}
$$

El demostrar que el determinante de esta matriz es 0 es a su vez demostrar que existe un unico punto critico $c=(c_{1},c_{2},\dots,c_{n})$ cuyo procedimiento queda fuera del dominio de este travajo (*me quede sin tiempo xd*).

Y una vez obtenido dicho punto $c$ se puede evaluar en la *matriz Heissiana* , obtener el determinante y usarlo como discriminante por el criterio de la segunda derivada parcial para demostrar que efectivamente el punto $c$ es un minimo local.



#### Procedimiento




para encontrar el polinomio de Lagrange dada por la sucesión de nodos, podemos utilizar el siguiente código 

```python
from numpy.polynomial.polynomial import Polynomial

poly_ols = Polynomial.fit(x_sample,y_sample,deg=26)

poly_ols.convert().coef[::-1]

```
que nos devuelve una clase polinomio que contiene los coeficientes de nuestro interes.


Grafcando el polinomio se obtuvo

!![Image Description](https://matutedevelop.github.io/blogg/images/Pasted%20image%2020250427121518.png)

un ajuste mucho mas adecuado


##### Coeficientes

$$


(1.391(10)^{+00})     
+ (2.669(10)^{-02}) x   
+ (-1.535(10)^{-01}) x^2 
+ (7.497(10)^{-02}) x^3   
+ (-1.333(10)^{-02}) x^4   
$$
$$
+ (1.229(10)^{-03}) x^5   
+ (-6.344(10)^{-05}) x^6   
+ (1.763(10)^{-06}) x^7   
+ (-2.177(10)^{-08}) x^8   
+ (4.852(10)^{-11}) x^9
$$



###  Lagrange vs OLS


Comparando los residuales se obtuvo una diferencia abrumadora  en el error.

!![Image Description](https://matutedevelop.github.io/blogg/images/Pasted%20image%2020250427122552.png)

Se sospecha que esta diferencia en el error es causada por el limite de la representacion de los decimales que tienen las computadoras. Esto debido a que teoricamente el polinomio de Lagrange deberia de tener error 0 al pasar por cada uno de los puntos. No obstante seguiria siendo un polinomio altamente *inestable* por ser de un grado elevado. 

Por otro lado con minimos cuadrados nosotros somos capaces de elegir el grado del polinomio y poder llegar asi a curvas mucho mas estables y suaves que nos generan sobre todo un mejor resultado.


## Integracion numerica

Una vez obtenido la funcion que modela la silueta de la botella toca calcular el volumen atraves de los metodos de integracion discutidos previamente

$$
A= \pi \int_{a}^b P^2(x)~dx
$$

Los polinomios tienen la virtud de ser bastante sencillos de integrar de forma simbolica. Ese no sera el procedimiento que usaremos nosotros.


### Regla del trapecio

#### Intuicion del metodo de  integracion numerica

Para entender de forma intuitiva la construccion de este metodo es pertinente revisitar la construccion informal de las sumas de Riemman.


$$A= \int_{a}^b f(x)~dx \approx \sum_{i=0}^n f(x_{i})\Delta x=A'$$ 

donde $x_{i}=a+i\Delta$ y se sabe que $A'\to A$ conforme $n \to \infty$.

Geometricamente lo que esto quiere decir es que la serie de las areas de los rectangulos  de ancho $\Delta x$ y altura $f(x_{i})$  converge al area total bajo la curva conforme se usan mas rectangulos.

![[Solidos de revolucion 2025-04-27 19.11.47.excalidraw|1000]]

Evidentemente trabajando con computadoras no podemos realizar un calculo o tarea un numero infinito de veces pero podemos hacerla un numero de veces suficientes para que la aproximacion sea satisfactoria. Pero tambien buscamos que el trabajo computacional invertido sea invertido de manera eficiente. Esto lo logramos realizando optimizaciones para minimizar el error en las sumas finitas. como por ejemplo cambiando los rctangulos por trapecios

![[Solidos de revolucion 2025-04-27 19.28.22.excalidraw|1000]]


entonces si deseamos aproximar de una mejor manera el area bajo la curva de $P$ reformulamos las sumas de riemman para sumar areas de trapecios en lugar de rectangulos.

El area del trapecio se obtiene de la siguiente manera

$$\frac{h}{2}(a_{1}+a_{2})$$

de donde $h$ es el largo del trapecio  y$a_{1},a_{2}$ las alturas de los trapecios

![[Solidos de revolucion 2025-04-27 19.58.03.excalidraw]]


#### Procedimiento

para aproximar el volumen del solido de revolucion se tiene que aproximar

$$\pi\int_{a}^bP^2(x)~dx$$

$a=0,b=\frac{49}{2}$ se desea dividir el intervalo en 10000 partes para calcular el area de 10000 trapecios

$$n=1000$$
$$\Delta x= \frac{b-a}{n}$$

$$x_{i}=a+i\Delta x,~~~~i=0,1,\dots,n-1$$
$$A_{i}=\frac{\Delta x}{2}((P(x_{i}))^2+(P(x_{i}+ \Delta x))^2),~~~~i=0,1,\dots,n-1$$

Donde $A_{i}$ es sucesion de los volumenes de los trapecios apartir del punto $x_{i}$.  

El volumen total del solido de revolucion es finalmente

$$
V=\pi \sum_{i=0}^{n-1}A_{i}
$$

> Nota: se uso dentro de la formula del trapecio $x_{i}+\Delta x$ en lugar de $x_{i+1}$ porque la serie esta definida en principio hasta $n-1$. Esto se escribio asi de forma que reflejara la forma exacta en la que el codigo fue implementado

##### Codigo 


###### Polinomio
```rust
use std::f64::consts::PI;

// Polinomio aproximador
fn p(x: f64) -> f64 {
    4.852272763781776e-11_f64 * x.powi(9)
    - 2.1769207076913663e-08_f64 * x.powi(8)
    + 1.76279592469982e-06_f64 * x.powi(7)
    - 6.344035947156883e-05_f64 * x.powi(6)
    + 0.0012285008019216523_f64 * x.powi(5)
    - 0.013329090419386656_f64 * x.powi(4)
    + 0.074970254828055_f64 * x.powi(3)
    - 0.15346857576947837_f64 * x.powi(2)
    + 0.026690674027164477_f64 * x
    + 1.3909550029629412_f64
    + - 0.4 // Ajuste por el grosor aproximado de la botella
}
```

###### Funcion area trapecio
```rust
fn area_trapecio(x1: f64, x2: f64, dx: f64, f: impl Fn(f64) -> f64) -> f64 {
    dx * (f(x1) + f(x2)) / 2.
}
```


###### Logica principal
```rust
fn main() {
	// Constantes
    let a = 0.0;
    let b = 24.5;
    let n = 10000;
    let dx = (b - a) / n as f64;

	// Integración
    let volumen = (0..n)
        .map(|i| a + i as f64 * dx)
        .map(|xi| area_trapecio(xi, xi + dx, dx,|x| p(x).powi(2)))
        .sum::<f64>() * PI;
    
    println!("El volumen del solido de revolucion es aproximadamente {}", volumen);
}
```


La lógica de este programa se implementó en el lenguaje de programación *Rust* por sus características *funcionales* que vienen de serie. La programacion funcional es un paradigma de programacion donde se evita el uso de ciclos `for` y la modificacion del *estado interno* de un programa. 
Este estilo de programacion nos permite *mapear* colecciones a colecciones sin necesidad de recorrer cada lista. Lo que da lugar a soluciones que pueden parecer un poco confusas en primer lugar, pero que en realidad son mas elegantes y sencillas.

lo que hace la linea despues de `//Integracion` es en esencia los siguientes mapeos 




$$
\usepackage{tikz-cd}
\usepackage{graphicx} 

\begin{document}
\scalebox{1}{
\begin{tikzcd}


i=0,1,...,n-1
\arrow[d, "a + i \Delta x"] \\
x_i \arrow[d, "\frac{h}{2}P(x_i)+P(x_{i+1})"] \\
A_i \arrow[d, "\pi \sum"] \\
V


\end{tikzcd}
}
\end{document}

$$

```tikz


\usepackage{tikz-cd}
\usepackage{graphicx} 

\begin{document}
\scalebox{1}{
\begin{tikzcd}


i=0,1,...,n-1
\arrow[d, "a + i \Delta x"] \\
x_i \arrow[d, "\frac{h}{2}P(x_i)+P(x_{i+1})"] \\
A_i \arrow[d, "\pi \sum"] \\
V


\end{tikzcd}
}
\end{document}

```


# Resultados

En primera instancia el volumen aproximado no fue bueno. Alrededor de 511 ml. Se presume que el grosor de la botella es de alrededor de 4 mm por lo que basto con integrar $P(x)-.04$ para llegar a una aaproximaciónmucho mas razonable de 369 mm, mucho mas cerca de los 355 ml mas el volumen de cuello de la botella


!![Image Description](https://matutedevelop.github.io/blogg/images/Pasted%20image%2020250427205723.png)


----

# Bibliografia

- https://static.sumaysigue.uchile.cl/disponibilizacion_aula360/G3D/U3%20-%20Generaci%C3%B3n%20de%20cuerpos%20utilizando%20patrones%20geom%C3%A9tricos/T2%20-%20Volumen%20de%20cuerpos%20geom%C3%A9tricos_/C1%20-%20Volumen%20y%20Principio%20de%20Cavalieri/Apunte%20Volumen%20y%20Principio%20de%20Cavalieri.pdf
- Curso_Teoria_Medida.pdf
- file:///C:/Users/fofoy/Downloads/ENTRETEXTOS-30-L2.pdf
- https://es.khanacademy.org/math/multivariable-calculus/multivariable-derivatives/partial-derivative-and-gradient-articles/a/the-gradient
- leithold
- https://www.khanacademy.org/math/multivariable-calculus/applications-of-multivariable-derivatives/quadratic-approximations/a/the-hessian 
- https://www.khanacademy.org/math/multivariable-calculus/applications-of-multivariable-derivatives/optimizing-multivariable-functions/a/second-partial-derivative-test
-  https://es.wikipedia.org/wiki/Corchete_de_Iverson
- https://www.cartagena99.com/recursos/alumnos/apuntes/DYCRE_1_T1_MaEm_U4L03.pdf