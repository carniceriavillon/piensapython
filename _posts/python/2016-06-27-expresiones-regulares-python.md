---
layout: default
intro: 'Pequeños lenguajes de programación'
title: Expresiones Regulares en Python
category: python
meta_contenido: expresiones regulares en python
date: 2016-06-26T10:20:00Z
---

<h1 class="centrar-titulo-blog">Expresiones Regulares en Python</h1>

(Actualizado para **PYTHON 3**)

Python 3 usa los conceptos de texto y datos binarios en lugar de cadenas Unicode y cadenas de 8 bits.
Todo texto en python 3 es Unicode y la codificación por defecto es utf-8. Incluso podemos usar nombres de 
variables con caracteres Unicode:
{% highlight python %}
>>> número = 98
>>> número + 78
176
{% endhighlight %}
Las expresiones regulares son como pequeños lenguajes de programación y su uso es conveniente cuando se trata 
de procesar cadenas de texto. Lo primero que hacemos en Python para trabajar con expresiones regulares 
es invocar al módulo:

{% highlight python %}
>>> import re
{% endhighlight %}

Algunas funciones de este módulo son: **compile, match, search, findall, split, sub, finditer**.

**COMPILE**:
Prepara el patrón de caracteres que se va a buscar. La sintaxis de compile es:

{% highlight python %}
>>> re.compile(pattern, flags=0)
{% endhighlight %}
pattern es el patrón de caracteres que se va a buscar y flags es el modificador que cambia el comportamiento del patrón. Esto es lo que hace cada modificador que aplicamos en compile.

**FLAGS**:

re.IGNORECASE (re.I) no distingue entre mayúsculas y minúsculas.

re.LOCALE (re.L) permite que algunos caracteres especiales tengan en cuenta el idioma que se usa en el
 computador local. Debido a que ahora se usa Unicode por defecto se recomienda usar este flag sólo con patrones de bytes.

re.MULTILINE (re.M) permite que "^" busque el comienzo de cada linea (no solo el comienzo del texto) y que "$" busque el final de cada linea (no solo el final del texto).
re.DOTALL (re.S) hace que "." busque cualquier caracter incluyendo una nueva linea (es decir '\n').

re.ASCII
Permite que  \w, \W, \b, \B, \d, \D, \s y \S busquen coincidencias ASCII en vez de Unicode.
Sólo es permitido para patrones Unicode e ignorado para bytes.

re.VERBOSE (re.X) se utiliza para poder dividir una expresión regular compleja en pequeños fragmentos que pueden tener comentarios para una mejor comprensión.
Si no se desea compilar pero sí usar modificadores, se puede usar el símbolo (?\_) junto con uno o varios modificadores, por ejemplo, (?i), (?m), (?iL).

A parte de la opción de usar modificadores compile ofrece una ligera mayor velocidad de búsqueda de los caracteres correspondientes. Un ejemplo de uso de compile:

{% highlight python %}
>>> pattern = re.compile('python', re.I)
>>> pattern.findall('la programación PyThOn')
['PyThOn']
{% endhighlight %}

Aqui con re.I se ignoran las mayúsculas y minúsculas lo que se puede lograr también sin compilar usando (?i):

{% highlight python %}
>>> re.findall('(?i)python','la programacion PyThOn')
['PyThOn']
{% endhighlight %}

De otra forma no hay correspondencia:

{% highlight python %}
>>> re.findall('python','la programacion Python')
[]
{% endhighlight %}

**MATCH**:
La función match determina si hay una coincidencia únicamente al comienzo del texto procesado:

{% highlight python %}
>>> patron = "Python"
>>> texto1 = "Monty Python"
>>> texto2 = "Python interpreter"
>>> match1 = re.match(patron, texto1)
>>> type(match1)  # no hay coincidencia
<type 'NoneType'>
>>> print match1
None
# python 3 muestra la coincidencia y los índices inicial y final
>>> match2 = re.match(patron, texto2)
<_sre.SRE_Match object; span=(0, 6), match='Python'> 
match2.group() # hay una coincidencia
'Python'
{% endhighlight %}

Incluso si se usa el modificador MULTILINE solamente hay búsqueda al comienzo del texto.

{% highlight python %}
>>> texto3 = "Monty \n Python"
>>> match3 = re.match(patron, texto3, re.M)# no hay coincidencia
{% endhighlight %}

**SEARCH**:
Busca la primera aparición del patrón de búsqueda en la cadena de texto. Search devuelve un objeto match o 
None si no hay coincidencia.

{% highlight python %}
>>> match = re.search('django', 'plataforma django, django reinhardt')
>>> match
<_sre.SRE_Match object; span=(11, 17), match='django'>
{% endhighlight %}

**FINDALL**:
Encuentra todas las coincidencias en forma de lista:

{% highlight python %}
>>> re.findall('\d+', '23 de junio, 14 de mayo')
['23', '14']
{% endhighlight %}

**FINDITER**:
Devuelve un iterador de objetos match. El resultado es igual a findall pero generando los elementos de la 
lista uno por uno.

{% highlight python %}
>>> iter_string = re.finditer('\d+', '23 de junio, 14 de mayo')
>>> iter_string
<callable-iterator object at 0x02ACE610>
# Usamos la funcón nativa next() para obtener el siguiente valor del iterador
>>> next(iter_string)
<_sre.SRE_Match object; span=(0, 2), match='23'>
>>> next(iter_string)
<_sre.SRE_Match object; span=(13, 15), match='14'>
{% endhighlight %}

**SUB**:
Sustituye el patrón por La sintaxis de sub es:

{% highlight python %}
>>> re.sub(pattern, repl, string, count=0, flags=0)

>>> re.sub('string', 'cadena', 'remplaza la string de caracteres')
'remplaza la cadena de caracteres'
{% endhighlight %}

**COUNT**: indica las veces que se debe sustituir el patrón de caracteres, por defecto se
remplazan todas las apariciones del texto.

{% highlight python %}
>>> re.sub('string', 'cadena', 'remplaza la string de caracteres string', count=1)
'remplaza la cadena de caracteres string'
{% endhighlight %}

**SUBN**: hace lo mismo pero devuelve una tupla con el número de remplazos.

{% highlight python %}
>>> re.subn('string', 'cadena', 'remplaza la string de caracteres string')
('remplaza la cadena de caracteres cadena', 2)
{% endhighlight %}

**SPLIT**:
Separa la cadena de texto en donde aparece el patrón.
{% highlight python %}
>>> re.split(pattern, string, maxsplit=0, flags=0)

>>> re.split('web','Django es un framework web de codigo abierto escrito en Python')
['Django es un framework ', ' de codigo abierto escrito en Python']
{% endhighlight %}
