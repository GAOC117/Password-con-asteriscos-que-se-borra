Este es un peque�o tutorial interactivo para mostrar y probar el uso de Markdown. Markdown es una sintaxis de conversi�n de texto a html empleada y soportada por Hup.me para a�adir descripciones en localizaciones, lugares y eventos. Este tutorial te permite directamente hacer pruebas y ver los resultados modificando directamente este texto y viendo los cambios que esto produce en la vista previa.

[Markdown](http://daringfireball.net/projects/markdown/) fue creado por John Gruber y Aaron Swartz con la filosof�a de formatear texto plano sin emplear marcas espec�ficas y �nicamente bas�ndose en las convenciones que la gente emplea al escribir en texto, por ejemplo en los emails

Sintaxis de Markdown
--------------------

Esta es una recopilaci�n de todos los elementos interpretados por Markdown

### P�rrafos y retornos de carro ##

Un p�rrafo es simplemente una o m�s l�neas de texto consecutivos
separados por una o m�s l�neas en blanco. Para separar el texto en p�rrafos
s�lo debes crear una l�nea en blanco como la que existe a continuaci�n.

Una l�nea en blanco no es otra cosa que una l�nea que s�lo contiene como mucho
espacios en blanco y/o tabulados.


### Encabezamientos ###

Markdown emplea dos tipos de sintaxis para los encabezamientos (etiquetas de cabecera de h1 a h6 en html)

Este es el encabezamiento m�s grande (h1)
=========================================

Este es un encabezamiento un poco m�s peque�o (h2)
--------------------------------------------------

La otra sintaxis es la siguiente

# Encabezamiento grande (h1)
## Encabezamiento m�s peque�o (h2)
###### El encabezamiento m�s peque�o (h6)

Tambi�n es v�lido

# Encabezamiento grande (h1) #
## Encabezamiento m�s peque�o (h2) ##
###### El encabezamiento m�s peque�o (h6) ######



### Bloques de citas ###

Markdown tambi�n soporta citas

> Esto es un bloque de citas
> puede extenderse varias l�neas
>
> He incluso por varios parrafos.
> S�lo es preciso agregar el s�mbolo
> mayor que al principio de cada l�nea.

Markdown tambi�n te permite incluir s�lo un > al principio de la primera l�nea de un parrafo

> Esto tambi�n es un bloque de cita
aunque solamente tenga un > en la l�nea inicial

> Este es otro p�rrafo de bloque de cita
empleando esta notaci�n

Bloques de citas pueden estar anidadas y contener adem�s otros elementos de Markdown. Mira el ejemplo de abajo

> #### Esto es un encabezamiento (h4)
>
> 1. Esto es el primer elemento de una lista
> 2. Este es el segundo elemento de una lista
>
> Aqu� hay un c�digo de bloque de cita anidado
>
> > Bloque anidado
>
> O un ejemplo de c�digo (para nuestros queridos programadores
>
>     return shell_exec("echo $input | $markdown_script");




### Listas ###

Markdown soporta listas ordenadas y no ordenadas.

Para crear una lista no ordenada use asteriscos (*), mases (+) o guiones (-)

* Blanco
* Amarillo
* Rojo
+ Azul
+ Verde
+ Violeta
- Marr�n
- Gris
- Negro

Las listas ordenadas deben ser n�meros seguidos de un punto (en realidad el valor del n�mero no importa y podr�a ser cualquiera, aunque el primer n�mero debe ser el 1)

1. Hup.me
2. Google.com
3. Yahoo.com
3. El valor de los n�meros
2. No es importante
1. Si el orden
0. En que se colocan los elementos

### Bloques de c�digo ###

El c�digo preformateado, generalmente empleado para escribir peque�os fragmentos de programas o c�digo que debe ser interpretado sin modificaciones se emplean los bloques de c�digo.

Para producir un bloque de c�digo en Markdow, solamente habr�a que a�adir al comienzo de cada l�nea del bloque de 4 espacios o un tabulador. Por ejemplo:

    Este es un bloque de c�digo
    Esta es la segunda l�nea del bloque

Dentro de un bloque de c�digo la sintaxis de Markdown no es procesada as� como tampoco lo es c�digo HTML. Por ejemplo:

    <div class="hola">
        mundo
    </div>

### L�neas horizontales ###

Puedes producir una l�nea separadora horizontal a�adiendo 3 o m�s guiones (-), asteriscos (*) o guiones bajos (_) solamente (aunque tambi�n podr�as a�adir espacios entre los guiones o los asteriscos)

* * *
***
*****
- - -
___________________________________


### Enlaces ###

Markdown soporta dos estilos de enlaces, que llamaremos, en l�nea y referencia.

En ambos estilos, el texto del enlace esta limitado por [corchetes]

Para crear un enlace en l�nea, usa los par�ntesis inmediatamente despu�s del corchete de cierre del texto del enlace. Dentro de estos par�ntesis, incluye la URL a donde debe apuntar el enlace, seguidamente puedes a�adir un t�tulo opcional entre comillas. Por ejemplo:

Esto es [un ejemplo](http://hup.me/ "T�tulo del ejemplo") de enlace en l�nea
Este otro [enlace](http://hup.me/contacta-con-nosotros) no tiene ning�n t�tulo

Puedes emplear tambi�n recursos locales del mismo servidor empleando rutas relativas.

Enlaces por referencias usan un segundo conjunto de corchetes. Dentro de los cuales se coloca la etiqueta empleada para identificar el enlace

Este es [un ejemplo][id] de un enlace por referencia.

Puedes utilizar un espacio entre los grupos de corchetes

Este es [un ejemplo] [id2] de un enlace por referencia.

En cualquier parte del documento puedes definir un enlace a la etiqueta como estos:

[id]: http://hup.me/ "T�tulo opcional"
[id2]: http://hup.me/contacta-con-nosotros "Contacta con nosotros"

* Los corchetes deben contener el identificador del enlace (opcionalmente identados con hasta 3 espacios como mucho)
* Seguidos de los dos puntos (:)
* Seguidos de uno o m�s espacios (o tabuladores)
* Seguidos de la URL del enlace.
* Y opcionalmente seguidos del t�tulo del enlace encerrados entre comillas dobles (") o entre par�ntesis.

La URL tambien puede estar encerrado entre parentesis angulares < >
[id3]: <http://hup.me/ayuda> (T�tulo opcional)

Puedes emplear el t�tulo en la siguiente l�nea y usar espacios adicionales o tabulaciones

[id4]: http://hup.me/terminos-y-condiciones
 "T�tulo opcional"

Estas definiciones de enlaces ser�n eliminados una vez que se procese el texto Markdown y no aparecer�n en el documento.

Puedes emplear el atajo de los *enlaces implicitos* que te permite omitir el nombre del enlace, en este caso el texto del enlace mismo sera el empleado para identificar el enlace. Simplemente emplea corchetes vacios. Por ejemplo

[Ayuda][]

Y en la definici�n del enlace

[Ayuda]: http://hup.me/ayuda

Las definiciones de enlaces pueden ser colocadas en cualquier lugar del documento.

### �nfasis ###

Mardown usa los asteriscos (*) y los guiones bajos (_) como indicadores de �nfasis. El texto envuelto por estos caracteres estar� enfatizado. Si el texto est� doblemente envuelto por estos indicadores el texto estar� m�s enfatizado y usualmente representado en negrilla.

*asteriscos simples*

_guiones bajos simples_

**asteriscos dobles**

__guiones bajos dobles__

El mismo car�cter debe ser empleado par envolver la palabra, la frase o la parte de la palabra. Si rodeas un asterisco o un gui�n bajo con espacios, ser� tratado de manera literal y no producir� �nfasis.

Tambi�n puedes evitar el �nfasis a�adiendo una barra invertido (\) a estos dos caracteres.

\*Este texto est� rodeado de asteriscos y no enfatizado\*

### C�digo ###

Para indicar un fragmento de c�digo dentro de una l�nea, sin emplear bloques de c�digo basta que emplees las comillas invertidas (`). Por ejemplo:

Usa la funci�n `printf()`.

Para incluir comillas invertidas dentro de una linea de c�digo, debes utilizar m�ltiples comillas invertidas como delimitadores

``Este es un ejemplo de una comilla invertida (`) dentro de una l�nea de c�digo``

Como en los bloques de c�digo puedes introducir c�digo HTML sin miedo a que este se interprete.

### Im�genes ###

Es dif�cil asignar una sintaxis "natural" para la colocaci�n de im�genes dentro de un texto.

Markdown emplea una sintaxis similar a la de los enlaces con 2 estilos: en l�nea y por referencia.

Ejemplos de im�genes en l�nea:

    ![Alt text](/ruta/a/la/imagen.jpg "T�tulo opcional")

![Logo de hup.me](/img/logo.png "Logo de hup.me")

Que sigue estas normas:

* Un signo de exclamaci�n (!)
* Seguido del atributo alt (texto alternativo) rodeado de corchetes
* Seguido de la url y t�tulo opcional entre comillas entre par�ntesis.

El estilo por referencia es an�logamente a lo que vimos para los enlaces:

![Texto alt][id-imagen]

La definici�n ser�a

[id-imagen]: /img/logo.png "Logo de hup.me"

### Miscel�nea ###

#### Enlaces autom�ticos ####

<http://hup.me/contacta-con-nosotros>

<contacto@hup.me>

#### Escapar con barras invertidas ####

\*Asteriscos literales\*

Markdown escapa con la barra invertida los siguientes caracteres

\\ barra invertida
\` comilla invertida
\* asterisco
\_ gui�n bajo
\{\} llaves
\[\] corchetes
\(\) parentesis
\# almohadillas
\+ signo m�s
\- signo menos o gui�n
\. punto
\! signo de exclamaci�n

