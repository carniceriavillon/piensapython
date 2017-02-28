---
layout: default
intro: 'Breve recuento de las listas por comprensión'
title: Listas y Diccionarios por Comprensión
category: python
meta_contenido: diccionarios y listas por comprension
date: 2016-06-27T10:20:00Z
---

<h1 class="centrar-titulo-blog">Listas y Diccionarios por Comprensión</h1>

Las listas por comprensión son análogas a los conjuntos por comprensión en teoría de conjuntos. Por ejemplo, A es el conjunto de las vocales (por comprensión) o A = {a,e,i,o,u} (por extensión).

En Python las listas por comprensión se expresan por medio de claúsulas for o if, por ejemplo, la lista A = [0,1,2,3,4] se expresa por comprensión como:

{% highlight python %}
A = [x for x in range(5)]
{% endhighlight %}

La primera parte de la lista es una expresión que se va a evaluar de acuerdo a las cláusulas if o for. Por ejemplo para obtener la lista de los números enteros múltiplos de 3 menores que 20:

{% highlight python %}
mult_3 = [x for x in range(1,20) if x%3 == 0]
print mult_3
[3, 6, 9, 12, 15, 18]
{% endhighlight %}

Este tipo de listas se pueden usar para resolver el primer problema del 
proyecto Euler(<a href="https://projecteuler.net/" target="_blank">Project Euler</a>):
<hr>
**MULTIPLES OF 3 AND 5.**

**Problem 1.**

If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23.
Find the sum of all the multiples of 3 or 5 below 1000.
<hr>

Por ejemplo, los números múltiplos de 5 menores que 20:

{% highlight python %}
[x for x in range(1,20) if x%5 == 0]
[5, 10, 15]
{% endhighlight %}

Los múltiplos de 3 menores que 20:

{% highlight python %}
[x for x in range(1,20) if x%3 == 0]
[3, 6, 9, 12, 15, 18]
{% endhighlight %}

La unión de estas dos listas sería:

{% highlight python %}
[x for x in range(1,20) if x%3 == 0 or x%5==0]
[3, 5, 6, 9, 10, 12, 15, 18]
{% endhighlight %}

Si usamos la misma notación para números menores que 1000:

{% highlight python %}
[x for x in range(1,1000) if x%3 == 0 or x%5==0]
{% endhighlight %}

Para hallar la suma podemos usar la función sum:

{% highlight python %}
sum([x for x in range(1,1000) if x%3 == 0 or x%5==0])
233168
{% endhighlight %}
