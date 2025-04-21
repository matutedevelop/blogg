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
> - *José C. Sabina de Lis* en 


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



|  yᵢ   | xᵢ   |
|:-----:|:----:|
| 1.40  | 0    |
| 1.30  | 1    |
| 1.25  | 2    |
| 1.35  | 3    |
| 1.45  | 4    |
| 1.65  | 5    |
| 1.95  | 6    |
| 2.35  | 7    |
| 2.55  | 8    |
| 2.75  | 9    |
| 2.89  | 10   |
| 3.00  | 11   |
| 3.05  | 12   |
| 3.10  | 13   |
| 3.13  | 14   |
| 3.05  | 15   |
| 2.90  | 16   |
| 2.80  | 17   |
| 2.70  | 18   |
| 2.60  | 19   |
| 2.55  | 20   |
| 2.70  | 21   |
| 3.05  | 22   |
| 3.15  | 23   |
| 2.85  | 24.5 |

Graficando se confirma efectivamente  asemejan la silueta de la botella partida a la mitad.

![[Pasted image 20250420131758.png|1000]]


## 2.2 Ajustando curva a los puntos

# Porque Lagrange vs MLS


- Lagrange se centra en interpolar en los puntos dados, es decir $P(x_{i})=y_{i}$, prioriza eso  y le vale madre el error






# Bibliografia

- https://static.sumaysigue.uchile.cl/disponibilizacion_aula360/G3D/U3%20-%20Generaci%C3%B3n%20de%20cuerpos%20utilizando%20patrones%20geom%C3%A9tricos/T2%20-%20Volumen%20de%20cuerpos%20geom%C3%A9tricos_/C1%20-%20Volumen%20y%20Principio%20de%20Cavalieri/Apunte%20Volumen%20y%20Principio%20de%20Cavalieri.pdf
- Curso_Teoria_Medida.pdf
- file:///C:/Users/fofoy/Downloads/ENTRETEXTOS-30-L2.pdf

