---
title: "Teorema de bayes"
date: "2025-02-26"
tags: 
summary: ""
description: ""
toc: true
readTime: true
autonumber: true
math: true
showTags: false
hideBackToTop: false

---
# Thomas Bayes

Nacido en *1702* hijo de uno de los primeros ministros presbiterianos ordenados el Inglaterra. Vivió su juventud en *St. Thomas* donde se especula que fue alumno de De Moivre, conocido por el teorema de  análisis complejo que lleva su nombre y por sus aportaciones con el teorema de De Moivre-Laplace que es un caso particular de él [[ CTL| Teorema del limite central]] que conecta la [[distribucion binomial]] con una [[distribucion normal]].

En 1719 ingresó a la universidad de Edimburgo, debido al impedimento a los alumnos presbiterianos a ingresar en universidades como Oxford o Cambridge. Ahí estudio Lógica y Teología.  Thomas Bayes fue ordenado al igual que su padre como ministro Presbiteriano y fue a estas actividades a la que les dedicaría la mayor parte de su vida.


## Impacto de su teorema

A pesar de no ser la rama del conocimiento en la que más tiempo de su vida dedicó, el teorema que lleva su nombre ofrece una herramienta profunda e importante para tratar con problemas clásicos de la teoría de la probabilidad. Tal es el caso del **problema de la probabilidad inversa.** Que fue una de las cuestiones fundamentales que dieron lugar a lo que hoy conocemos como **Estadística inferencial**.




### Probabilidad inversa

El problema de la probabilidad inversa consiste en encontrar la *distribución* de una variable no observada


# Versión original del teorema de bayes 

La publicación del que fue irrefutablemente su mejor trabajo fue hecho después de su muerte, a manos de *Richard Price*, un amigo de Thomas que pertenecía a la *Royal Society* (Revista en la que se publicaría el trabajo de Bayes) y que era trabajaba como experto de administración de riesgos de seguros. Él fue el encargado de terminar de editar y presentar ante la *Royal Society* un ensayo titulado *[An Essay towards solving a Problem in the Doctrine of Chances](https://royalsocietypublishing.org/doi/pdf/10.1098/rstl.1763.0053),* donde se presentaría el siguiente postulado.

!![Image Description](https://matutedevelop.github.io/blogg/images/Pasted%20image%2020250319184634.png)

Que en una notación moderna vendría a decir lo siguiente

Dado $P(B)=\frac{b}{N},P(A \cap B) = \frac{P}{N}$ entonces $P(A|B)=\frac{P(A\cap B)}{P(B)}=\frac{\frac{P}{N}}{\frac{b}{N} } = \frac{P}{b}$

Esto luce bastante alejado a o que hoy conocemos como el teorema de Bayes, pero el tema es que el teorema de Bayes es una consecuencia bastante directa de esta definición, y es en esta verdad  numérica en donde yace todo el impacto y la importancia de los trabajos de bayes. Que derivarían en una revolución casi filosófica de las concepciones de probabilidad, en las cuales el pensamiento de la [escuela frecuentista](https://www.youtube.com/watch?v=8wVq5aGzSqY&t=489s) había y sigue siendo imperante. 



# Versión moderna del teorema de Bayes

La versión que conocemos hoy como el teorema de valles es un teorema comletamente enfocado como a herramienta para resolver problemas de probabilidad inversa


> [! Danger] # $\aleph~~\mathbb{T}\mathrm{eorema}$ 
> #MATH/THEOREM 
> 
> El teorema de **bayes** enuncia lo siguiente
> $$P(B|A) =\frac{P(A|B)P(B)}{P(A)}$$




##### Bibliografia 


- https://www.sciencedirect.com/topics/computer-science/inverse-probability
- https://www.ugr.es/~eaznar/bayes.html
- https://higherlogicdownload.s3.amazonaws.com/AMSTAT/1484431b-3202-461e-b7e6-ebce10ca8bcd/UploadedImages/Classroom_Activities/HP_4_Inverse_Probability_-_Thomas_Bayes.pdf
- https://www.youtube.com/watch?v=8wVq5aGzSqY&t=489s
- https://royalsocietypublishing.org/doi/pdf/10.1098/rstl.1763.0053