Este es un pequeño tutorial interactivo para mostrar y probar el uso de Markdown. Markdown es una sintaxis de conversión de texto a html empleada y soportada por Hup.me para añadir descripciones en localizaciones, lugares y eventos. Este tutorial te permite directamente hacer pruebas y ver los resultados modificando directamente este texto y viendo los cambios que esto produce en la vista previa.

[Markdown](http://daringfireball.net/projects/markdown/) fue creado por John Gruber y Aaron Swartz con la filosofía de formatear texto plano sin emplear marcas específicas y únicamente basándose en las convenciones que la gente emplea al escribir en texto, por ejemplo en los emails

Sintaxis de Markdown
--------------------

Esta es una recopilación de todos los elementos interpretados por Markdown

### Párrafos y retornos de carro ##

Un párrafo es simplemente una o más líneas de texto consecutivos
separados por una o más líneas en blanco. Para separar el texto en párrafos
sólo debes crear una línea en blanco como la que existe a continuación.

Una línea en blanco no es otra cosa que una línea que sólo contiene como mucho
espacios en blanco y/o tabulados.


### Encabezamientos ###

Markdown emplea dos tipos de sintaxis para los encabezamientos (etiquetas de cabecera de h1 a h6 en html)

Este es el encabezamiento más grande (h1)
=========================================

Este es un encabezamiento un poco más pequeño (h2)
--------------------------------------------------

La otra sintaxis es la siguiente

# Encabezamiento grande (h1)
## Encabezamiento más pequeño (h2)
###### El encabezamiento más pequeño (h6)

También es válido

# Encabezamiento grande (h1) #
## Encabezamiento más pequeño (h2) ##
###### El encabezamiento más pequeño (h6) ######



### Bloques de citas ###

Markdown también soporta citas

> Esto es un bloque de citas
> puede extenderse varias líneas
>
> He incluso por varios parrafos.
> Sólo es preciso agregar el símbolo
> mayor que al principio de cada línea.

Markdown también te permite incluir sólo un > al principio de la primera línea de un parrafo

> Esto también es un bloque de cita
aunque solamente tenga un > en la línea inicial

> Este es otro párrafo de bloque de cita
empleando esta notación

Bloques de citas pueden estar anidadas y contener además otros elementos de Markdown. Mira el ejemplo de abajo

> #### Esto es un encabezamiento (h4)
>
> 1. Esto es el primer elemento de una lista
> 2. Este es el segundo elemento de una lista
>
> Aquí hay un código de bloque de cita anidado
>
> > Bloque anidado
>
> O un ejemplo de código (para nuestros queridos programadores
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
- Marrón
- Gris
- Negro

Las listas ordenadas deben ser números seguidos de un punto (en realidad el valor del número no importa y podría ser cualquiera, aunque el primer número debe ser el 1)

1. Hup.me
2. Google.com
3. Yahoo.com
3. El valor de los números
2. No es importante
1. Si el orden
0. En que se colocan los elementos

### Bloques de código ###

El código preformateado, generalmente empleado para escribir pequeños fragmentos de programas o código que debe ser interpretado sin modificaciones se emplean los bloques de código.

Para producir un bloque de código en Markdow, solamente habría que añadir al comienzo de cada línea del bloque de 4 espacios o un tabulador. Por ejemplo:

    Este es un bloque de código
    Esta es la segunda línea del bloque

Dentro de un bloque de código la sintaxis de Markdown no es procesada así como tampoco lo es código HTML. Por ejemplo:

    <div class="hola">
        mundo
    </div>

### Líneas horizontales ###

Puedes producir una línea separadora horizontal añadiendo 3 o más guiones (-), asteriscos (*) o guiones bajos (_) solamente (aunque también podrías añadir espacios entre los guiones o los asteriscos)

* * *
***
*****
- - -
___________________________________


### Enlaces ###

Markdown soporta dos estilos de enlaces, que llamaremos, en línea y referencia.

En ambos estilos, el texto del enlace esta limitado por [corchetes]

Para crear un enlace en línea, usa los paréntesis inmediatamente después del corchete de cierre del texto del enlace. Dentro de estos paréntesis, incluye la URL a donde debe apuntar el enlace, seguidamente puedes añadir un título opcional entre comillas. Por ejemplo:

Esto es [un ejemplo](http://hup.me/ "Título del ejemplo") de enlace en línea
Este otro [enlace](http://hup.me/contacta-con-nosotros) no tiene ningún título

Puedes emplear también recursos locales del mismo servidor empleando rutas relativas.

Enlaces por referencias usan un segundo conjunto de corchetes. Dentro de los cuales se coloca la etiqueta empleada para identificar el enlace

Este es [un ejemplo][id] de un enlace por referencia.

Puedes utilizar un espacio entre los grupos de corchetes

Este es [un ejemplo] [id2] de un enlace por referencia.

En cualquier parte del documento puedes definir un enlace a la etiqueta como estos:

[id]: http://hup.me/ "Título opcional"
[id2]: http://hup.me/contacta-con-nosotros "Contacta con nosotros"

* Los corchetes deben contener el identificador del enlace (opcionalmente identados con hasta 3 espacios como mucho)
* Seguidos de los dos puntos (:)
* Seguidos de uno o más espacios (o tabuladores)
* Seguidos de la URL del enlace.
* Y opcionalmente seguidos del título del enlace encerrados entre comillas dobles (") o entre paréntesis.

La URL tambien puede estar encerrado entre parentesis angulares < >
[id3]: <http://hup.me/ayuda> (Título opcional)

Puedes emplear el título en la siguiente línea y usar espacios adicionales o tabulaciones

[id4]: http://hup.me/terminos-y-condiciones
 "Título opcional"

Estas definiciones de enlaces serán eliminados una vez que se procese el texto Markdown y no aparecerán en el documento.

Puedes emplear el atajo de los *enlaces implicitos* que te permite omitir el nombre del enlace, en este caso el texto del enlace mismo sera el empleado para identificar el enlace. Simplemente emplea corchetes vacios. Por ejemplo

[Ayuda][]

Y en la definición del enlace

[Ayuda]: http://hup.me/ayuda

Las definiciones de enlaces pueden ser colocadas en cualquier lugar del documento.

### Énfasis ###

Mardown usa los asteriscos (*) y los guiones bajos (_) como indicadores de énfasis. El texto envuelto por estos caracteres estará enfatizado. Si el texto está doblemente envuelto por estos indicadores el texto estará más enfatizado y usualmente representado en negrilla.

*asteriscos simples*

_guiones bajos simples_

**asteriscos dobles**

__guiones bajos dobles__

El mismo carácter debe ser empleado par envolver la palabra, la frase o la parte de la palabra. Si rodeas un asterisco o un guión bajo con espacios, será tratado de manera literal y no producirá énfasis.

También puedes evitar el énfasis añadiendo una barra invertido (\) a estos dos caracteres.

\*Este texto está rodeado de asteriscos y no enfatizado\*

### Código ###

Para indicar un fragmento de código dentro de una línea, sin emplear bloques de código basta que emplees las comillas invertidas (`). Por ejemplo:

Usa la función `printf()`.

Para incluir comillas invertidas dentro de una linea de código, debes utilizar múltiples comillas invertidas como delimitadores

``Este es un ejemplo de una comilla invertida (`) dentro de una línea de código``

Como en los bloques de código puedes introducir código HTML sin miedo a que este se interprete.

### Imágenes ###

Es difícil asignar una sintaxis "natural" para la colocación de imágenes dentro de un texto.

Markdown emplea una sintaxis similar a la de los enlaces con 2 estilos: en línea y por referencia.

Ejemplos de imágenes en línea:

    ![Alt text](/ruta/a/la/imagen.jpg "Título opcional")

![Logo de hup.me](/img/logo.png "Logo de hup.me")

Que sigue estas normas:

* Un signo de exclamación (!)
* Seguido del atributo alt (texto alternativo) rodeado de corchetes
* Seguido de la url y título opcional entre comillas entre paréntesis.

El estilo por referencia es análogamente a lo que vimos para los enlaces:

![Texto alt][id-imagen]

La definición sería

[id-imagen]: /img/logo.png "Logo de hup.me"

### Miscelánea ###

#### Enlaces automáticos ####

<http://hup.me/contacta-con-nosotros>

<contacto@hup.me>

#### Escapar con barras invertidas ####

\*Asteriscos literales\*

Markdown escapa con la barra invertida los siguientes caracteres

\\ barra invertida
\` comilla invertida
\* asterisco
\_ guión bajo
\{\} llaves
\[\] corchetes
\(\) parentesis
\# almohadillas
\+ signo más
\- signo menos o guión
\. punto
\! signo de exclamación

