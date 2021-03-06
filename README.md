# css
Practica de CSS con lo mas utilizado:
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

CSS significa Cascading Style Sheets traducido como hojas de estilo en cascada. Es el lenguaje de estilos que se utiliza para la presentacion de documentos HTML. Una particularidad es que los estilos que  escribo abajo sobreescriben a los de arriba.
 Para utilizar CSS en nuestro HTML existen varias formas como:
 * utilizar la etiqueta link <link rel="stylesheet" href=""> esta etiqueta conecta el html con el css externo, en la misma u otra carpeta.
 *utilizar el atributo style dentro del HTML <style></style> en el head, se usa generalmente en la creación o maquetación de correos electronicos
 *usar el atributo style en linea, es decir aplicarlo al elemento que se quiere aplicar estilos, no es recomendable su utilización.
 *usar @import url(css/styles.css) que equivaldria a link, pero solo guarda si se guardan los cambios en el HTML, se carga de forma asincrona. Tampoco es recomendable esta practica.
  
En CSS se encuentran elementos como:
*selector: elemento al que vamos a plicar estilos.
*propiedad: lo que vamos a cambiar.
*valor: el nuevo valor que le vamos a dar a la propiedad.
*propiedad:valor -> se le denomina declaracion
*al conunto de selector+declaracion(es) se le denomina regla.
ejemplo:
selector{
    propiedad:valor;
}
 body {
    background-color:steelblue;
}
    selectores:
selectores simples y compuestos: dentro de los selectores simples se encuentran los selectores elementales y los de atributo, a su vez en los elementales se subdivide en selector universal(* representa el documento entero) y selector de tipo o etiqueta(poner el nombre de la etiqueta), los seklectores de atributo se subdivide en id(id del elemento), clase(clase del elemento), y otros atributos([atributo],[atributo=valor],[atributo^=valor], [atributo*=valor], [atributo$=valor], [atributo|=valor]); y en los compuestos se encuentran los selectores agrupados, los combinadores, las pseudoclases y los pseudoelementos.
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
*Teoria de CSS*

Margin: es la propiedad que nos permite generar espacio entre elementos(en el box model separa las cajas). Es un shorthand que controla los 4 lados posibles a los que dar margenes. Admite hasta 4 valores que van en el orden de las agujas del reloj(top right bottom left) los elementos de linea solo tienen margin horizontal. si usamos margin left/right: auto la caja se pega al borde opuesto.Errores comunes: usar el *{
          margin:0; padding:0; y margin:0 auto; en vez de eso usar margin-left y right auto; margin:0 en el body si esta bien ya que por defecto tiene 8px.  }
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Padding: es el espacio entre el contenido de la caja y el borde. 4 valores posibles, idem que margin.
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Border: es la propiedad que nos permite modificar el borde de la caja. agrupa 3 propiedades border-width el ancho del borde; border-style: estilo del borde; y border-color: color del borde;
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Box sizing: es la propiedad que nos permite controlar el calculo que hace el navegador a la hora de modificar: content, padding y border. Con el box-sizing:border box aplica el calculo automaticamente del padding y border. Si aplico el selector universal para que todas las cajas tengan el border-box es una practica correcta.
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Border-radius: permite redondear los bordes de una caja. engloba 4 propiedades: Border-top-left-radius radio del borde superior izquierdo; border-top-right-radius radio del borde superior derecho; border-bottom-right-radius borde inferior derecho; y border-bottom-left-radius borde inferior izquierdo. Si solo recibe un valor dibujara un circulo en cada vertice del radio que especifiquemos.
        si utilizamos border-top-left-radius y le asignamos 2 valores toma la forma de una elipse y no de un circulo. Ejemplo: border-radius: 50px / 100px;
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Overflow: es la propiedad que controla que debe hacer la caja cuando su contenido se desborda del contenedor. Es un shorthand que engloba overflow-x y overflow-y. tiene 4 posibles valores. visible(por defecto); hidden el contenido que se desborde no se vera si se aplica en un solo eje, el otro automaticamente se pone en scroll; scroll apareceran barras de scroll en el eje asignado (x, y o ambos); y auto apareceran barras de scroll en el caso de ser necesarias.
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Colapsado de margenes: los margenes verticales se solapan.
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Display: Nos sirve para cambiar el contexto de los elementos del navegador. Admite varios valores como: none (hace que el elemento no se muestre, pero sigue cargandose); block (hace que el elemento sea de bloque); inline(hace que el elemento sea de linea); inline-block (hace que el elemento sea de linea pero admite medidas y margenes verticales);
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Outline: es la propiedad que nos permite dibujar un borde por fuera del modelo de la caja. es un shorthand que engloba: outline-width(que controla el ancho de outline); outline-style(que controla el estilo del outline); outline-color(que controla el color del outline). Tiene las mismas propiedades y sintaxis que el border pero con algunas diferencias como que no ocupa sitio, ya que no forma parte del box-model, no se puede redondear y no se pueden controlar los lados de forma independiente. Tambien cuenta con la propiedad outline-offset que nos permite aumentar o disminuir la distancia del outline en relacion a la caja a la que pertenece.
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Text-align: Es la propiedad que nos permite alinear horizontalmente el contenido de un elemento de bloque simepre que el contenido NO TENGA ANCHO DECLARADO. Acepta 4 valores: text-align:left alinea el contenido a la izquierda, es la propiedad por defecto; text-align:right alinea el contenido a la derecha; text-align:center alinea el contenido al centro, solo centra elementos de contenido en bloque, por lo que si fuera un link habria que darle display: block; text-align: justify alinea el contenido de forma justificada. No es recomendable usarlo. Pra centrar una caja o una imagen es conveniente usar Margin-left: auto y margin-right:auto y si fuera un contenido como imagen dentro de un div al aplicarle text-align: center se centra.
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Box-shadow: se creo para añadir efectos de sombra a nuestra caja. En esencia lo que hace es crear un clon de la caja respetando la forma de su box-model (ancho, alto, redondez). La sintaxis de box-shadow se puede escribir de distintas formas lo que queremos conseguir. Los valores que le podemos poner son: offset-x desplazamiento en x (obligatorio); offset-y desplazamiento en y (obligatorio); blur-radius desenfoque de la sombra; color el color de la sombra, si no lo especificamos lo heredara del elemento al que pertenece; inset determina si la sombra sera interior o exterior;
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Position: nos permite posicionar los elementos. Flujo de renderizado: por norma general los elementos se dibujan de izquierda a derecha y de arriba abjo. El punto 0, 0 de los elementos por norma general es la esquina superior izquierda; Espacio reservado: es el espacio que tiene un elemento asignado en el navegador. Elemento posicionado: esto significa que el elemento tiene la propiedad position con un valor distinto de "static", que es el valor que tiene esta propiedad por defecto; Stacking context: contexto de apilamiento. Es el orden en el que se apilaran las cajas que lo superponen. A l posicionar un elemento se habilitan 5 propiedades que podemos utilizar para mover los elementos en los 3 ejes. top (el elemento se movera desde la parte superior la distancia que le hayamos indicado), right (el elemento se movera desde la parte derecha la distancia que le hayamos indicado), bottom (el elemento se movera desde la parte inferior la distancia que le hayamos indicado), left (el elemento se movera desde la parte izquierda la distancia que le hayamos indicado), z-index (nos permite mover el elemento en el contexto de apilamiento, eje z). Si a un elemento le declaramos la propiedad top y/o left, las propiedades bottom y/o right no funcionaran.
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Los posibles valores que le podemos dar a position son: static(es el valor que tiene por defecto un elemento, con este valor el elemento NO ESTA POSICIONADO y por lo cual no podremos moverlo); relative( el elemento se mantendra su posicion y medidas en el flujo de renderizado y mantendra su espacio reservado. Si lo movemos lo hara usando su posicion en el html como punto de referencia); absolute(el elemento perdera sus medidas y su espacio reservado. Si lo movemos usara el elemento padre posicionado como referencia. Si no tiene ninguno, usara el elemento html de referencia), fixed(el elemento perdera sus medidas y su espacio reservado. S i lo movemos usara el elemento html de referencia y ademas se quedara fijo en esa posicion aunque le hagamos scroll), sticky(es una mezcla de position relative y fixed. Con este tipo de posicionamiento los valores top, left, bottom y right no sirven para mover el elemento, si no para indicarle en que punto pasara a tener un comportamiento de posicionamiento fixed, hasta llegar a ese punto se comportara como si tuviera relative).
Cuando usamos posicion absolute pierde sus medidas y pierde el espacio reservado.



Elementos en linea y en bloque:
Los elementos en linea ocupan el lugar que ocupa su contenido.
No se le puede dar medidas a un elemento en linea(inline)

BEM es una convención o metodología para nombrar tus clases de CSS. Por sus siglas en inglés, BEM significa Bloque, Elemento y Modificador.

En esta guía aprenderemos:

Cómo funciona BEM
Cómo usar BEM en CSS
Por qué y para qué usar BEM
Ejemplo prácticos de BEM (incluyendo un cohete Falcon 9 de Space X) 🚀
3 casos con lo que debes y no debes hacer con BEM
3 problemas comunes en BEM y cómo solucionarlos
BEM + SASS
Recomendaciones finales
¿Cómo funciona BEM?
BEM funciona identificando el bloque, el elemento y el modificador de un componente.

Bloque es el contenedor principal del componente.
Elemento son las partes internas que conforman el componente.
Modificador son las variaciones del bloque o del elemento.
El cohete Falcon 9 de SpaceX está compuesto por varias partes que hacen posible el transporte confiable y seguro de personas o cargas útiles a la órbita terrestre (incluso más allá). Para cada una de las partes podemos crear una analogía
Teniendo entonces:

Bloque: Falcon 9
Elementos: First stage, Interstage, Second stage.
Modificador: Fairing, Dragon.
Después de revisar la analogía con el cohete Falcon 9, revisemos algunos ejemplos que podemos encontrarnos en la vida real:

Bloque: card, button, form, menu, header…
Elemento: icon, text, item, image, input, button…
Modificador: active, big, right, secondary, red…
😍

Cómo se usar BEM en CSS
Los nombres de clases con convención BEM,pueden tener la siguiente sintaxis:

[bloque]
[bloque]__[elemento]
[bloque]--[modificador]
[elemento]--[modificador]
[bloque]__[elemento]--[modificador]
Teniendo en cuenta lo anterior, el CSS para nuestro Falcon 9 se escribiría así:

.falcon9 { ... }
.falcon9--fairing { ... }
.falcon9--dragon { ... }
.falcon9__first-stage { ... }
.falcon9__interstage { ... }
.falcon9__second-stage { ... }
Y así se vería el HTML:

<rocket class="falcon9 falcon9--dragon">
    <stage class="falcon9__first-stage"></stage>
    <stage class="falcon9__interstage"></stage>
    <stage class="falcon9__second-stage"></stage>
</rocket>
Además, el CSS siguiendo BEM con un ejemplo de la vida real se escribiría así:

.button { ... }
.button--active { ... }
.button__icon { ... }
.button__text { ... }
Y así se vería el HTML:

<button class="button button--active">
    <i class="button__icon"></i>
    <span class="button__text"></span>
</button>
⚠️ Importante: recuerda que:

Los guiones bajos (__) se usan para separar el bloque del elemento,
Los guiones medios (--) se usan para separar el bloque o el elemento del modificador.
💡 Nota: BEM permite cambiar esta nomenclatura. También puedes encontrar nombres de clase así: [bloque]__[elemento]-[modificador], [bloque]__[elemento]_[modificador], entre otros. Lo más importante a la hora de usar una de estas nomenclaturas es ser consistente en todo el proyecto.

¿Por qué y para qué usar BEM?
Tal vez te preguntes, “Pero, ¿Teff, para qué seguir esta metodología si el resultado en CSS es el mismo? ¡Solo estamos haciendo más trabajo!”

Para tener un CSS más fácil de leer, entender, mantener y escalar.
Para organizar las clases de CSS en módulos independientes.
Para evitar selectores de CSS anidados.
Casos prácticos de BEM
Card:
Identifiquemos el bloque, los elementos y los modificadores (si los tiene) de la siguiente card:
De la imagen anterior, tenemos lo siguiente:

Bloque: card
Elementos: image, text
Modificadores: (no tiene)
Su estructura de HTML con la convención de clases BEM, sería:

<div class="card">
    <img class="card__image" src="/image.png" alt="spacesuit" />
    <p class="card__text"></p>
    <p class="card__text"></p>
</div>
Navbar:
Identifiquemos el bloque, los elementos y los modificadores (si los tiene) del siguiente navbar:
De la imagen anterior, tenemos lo siguiente:

Bloque: navbar
Elementos: logo, items
Modificadores: gray
Su estructura de HTML con la convención de clases BEM, sería:

<nav class="navbar">
    <ul class="navbar">
        <li class="navbar__item"><i class="navbar__icon"></i></li>
        <li class="navbar__item">MENS</li>
        <li class="navbar__item">WOMENS</li>
        <li class="navbar__item">KIDS</li>
        <li class="navbar__item">ACCESSORIES</li>
        <li class="navbar__item">PREMIUM</li>
        <li class="navbar__item navbar__item--gray">ACCOUNT</li>
        <li class="navbar__item navbar__item--gray">SEARCH</li>
        <li class="navbar__item">CART (0)</li>
    </ul>
</nav>
Section:
Identifiquemos el bloque, los elementos y los modificadores (si los tiene) de la siguiente sección:
Como de la imagen anterior identificamos 2 bloques, vamos a dividir la estructura en 2 partes, así:

Para el bloque 1:

Bloque: section
Elementos: text, image
Modificadores: primary, secondary-semibold, secondary-bold
Para el bloque 2:

Bloque: list
Elementos: item, text
Modificadores: gray
La estructura de HTML con la convención de clases BEM para ambos bloques, sería:

<section class="section">
    <div>
        <h2 class="section__text section__text--primary">FALCON 9</h2>
        <p class="section__text section__text--secondary-semibold">Falcon 9, the world's first orbital class reusable rocket...</p>
        <p class="section__text section__text--secondary-bold">Learn more about Falcon 9</p>
        <ul class="list">
            <li class="list__item">
                <span class="list__text">VEHICLE HEIGHT</span>
                <div>
                    <span class="list__text">70m</span>
                    <span class="list__text list__text--gray">/229.6 ft</span>
                </div>
            </li>
            <li class="list__item">
                <span class="list__text">VEHICLE DIAMETER</span>
                <div>
                    <span class="list__text">3.7m</span>
                    <span class="list__text list__text--gray">/12 ft</span>
                </div>
            </li>
            <li class="list__item">
                <span class="list__text">FAIRING HEIGHT</span>
                <div>
                    <span class="list__text">13.1m</span>
                    <span class="list__text list__text--gray">/43 ft</span>
                </div>
            </li>
            <li class="list__item">
                <span class="list__text">FAIRING DIAMETER</span>
                <div>
                    <span class="list__text">5.2m</span>
                    <span class="list__text list__text--gray">/17.1 ft</span>
                </div>
            </li>
        </ul>
    </div>
    <div>
    </div>
    
</section>
Casos con lo que debes y no debes hacer con BEM
1️⃣ Primer caso
Lo que sí: dejar la clase principal card y añadir otra clase con modificador.
<div class="card card--flat"></div>
Lo que no: usar la clase con modificador como clase principal.
<div class="card--flat"></div>
2️⃣ Segundo caso
Lo que sí: no representar los niveles de profundidad de HTML con BEM.
<div class="card">
    <img class="card__image" src="/image.png" alt="Crew Dragon" />
    <p class="card__text">
        <i class="card__icon">
    </p>
</div>
Lo que no: representar los niveles de profundidad de HTML con BEM.
<div class="card">
    <img class="card__image" src="/image.png" alt="Crew Dragon" />
    <p class="card__text">
        <i class="card__text__icon">
    </p>
</div>
3️⃣ Tercer caso
Lo que sí: incluir la clase en un hijo que necesita estilos.
<div class="card">
    <img class="card__image" src="/image.png" alt="Crew Dragon" />
</div>

<style>
    .card { ... }
    .card__image { ... }
</style>
Lo que no: Omitir la clase en un hijo que necesita estilos.
<div class="card">
    <img src="/image.png" alt="Crew Dragon" />
</div>

<style>
    .card { ... }
    .card img { ... }
</style>
3 problemas comunes con BEM y cómo solucionarlos
1️⃣ Primer caso
Problema: tengo un componente A que ya tiene sus propias clases y deseo añadirlo a un nuevo componente B. ¿Debo agregar una nueva convención para el componente A que estará dentro de B?
Componente A:

<button class="button button--active"></button>
Componente B:

<div class="card">
    <img class="card__image" src="/image.png" alt="Crew Dragon" />
</div>
Solución: puedes dejar el componente A con las clases que ya estaban establecidas así no sean coherentes con el nuevo componente B, por ejemplo:
<div class="card">
    <img class="card__image" src="/image.png" alt="Crew Dragon" />
    <button class="button button--active"></button>
</div>
2️⃣ Segundo caso
Problema: en mi estructura de HTML tengo padres, hijos, nietos, tataranietos, etc; pero BEM sólo me deja usar 3 niveles. ¿Qué hago con los elementos nietos y sus descendientes?
<div class="card">
    <img class="card__image" src="/image.png" alt="Crew Dragon" />
    <div class="card__footer">
        <p class="card__footer__text">
            <i class="card__footer__text__icon">
        <p>
    </div>
</div>
Solución: como lo mencionamos anteriormente, BEM no representa los niveles de tu estructura de HTML. Lo ideal en este caso sería tener:
<div class="card">
    <img class="card__image" src="/image.png" alt="Crew Dragon" />
    <div class="card__footer">
        <p class="card__text">
            <i class="card__icon">
        <p>
    </div>
</div>
3️⃣ Tercer caso
Problema: quiero utilizar la propiedad display: none para ocultar desde JavaScript un componente de Card y un componente de Botón. ¿Debo crear una clase para cada componente siguiendo su propia estructura de BEM (card--hidden y button--hidden)?
<div class="card card--hidden">
    <img class="card__image" src="/image.png" alt="Crew Dragon" />
</div>
<button class="button button--hidden"></button>

<style>
    .card--hidden {
        display: none;
    }
    .button--hidden {
        display: none;
    }
</style>
Solución: puedes crear una clase independiente a la estructura de BEM para aplicar propiedades generales, así, reducirás la cantidad de líneas de JavaScript ya que no tendrás que usar una clase específica para cada componente.
<div class="card hidden">
    <img class="card__image" src="/image.png" alt="Crew Dragon" />
</div>
<button class="button hidden"></button>

<style>
    .hidden {
        display: none;
    }
</style>
• BEM + SASS
Dragon es la primera nave espacial privada en llevar humanos a la estación espacial. Pero, no lo hace sola. Dragon trabaja en conjunto con el cohete Falcon 9 para tener un lanzamiento perfecto.
Así como Dragon y Falcon 9 trabajan juntos, BEM y SASS también. SASS es un preprocesador de CSS que te permite anidar selectores, crear bucles, funciones, entre otras cosas. Y, adicionalmente, gracias a la sintaxis de SASS, podemos tener una combinación perfecta en nuestras hojas de estilos.

Por ejemplo, uno de nuestros ejercicios anteriores fue el siguiente:

<div class="card">
    <img class="card__image" src="/image.png" alt="Crew Dragon" />
    <button class="button button--active"></button>
</div>
Donde, el CSS se ve de la siguiente forma:

.card {
    ...
}
.card__image {
    ...
}
.button {
    ...
}
.button--active {
    ...
}
Pero si usamos SASS, nuestros estilos se verían de la siguiente forma:

.card {
    &__image {
        ...
    }
}
.button {
    &--active {
        ...
    }
}
Aquí sólo alcanzamos a reducir 2 líneas de código, pero, ¿te alcanzas a imaginar cuántas líneas de código podríamos ahorrarnos en un proyecto con mucho más HTML y CSS? Este es uno de los súper poderes de combinar BEM con SASS, aparte de que se ve mucho más lindo y limpio nuestro código.

Recomendaciones finales
Los proyectos que usan BEM son fáciles de leer, muy intuitivos y permiten evitar los selectores de CSS anidados. También, es una herramienta que permite personalizar las reglas y nomenclatura para tener un código mucho más limpio y escalable.




