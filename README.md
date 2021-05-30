# css
practica de css con lo mas utilizado:
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
selectores simples y compuestos: dentro de los selectores simples se encuentran los selectores elementales y los de atributo, a su vez en los elementales se subdivide en selector universal(* representa el documento entero) y selector de tipo o etiqueta(poner el nombre de la etiqueta), los seklectores de atributo se subdivide en id(id del elemento), clase(clase del elemento), y otros atributos([atributo],[atributo=valor],[atributo^=valor], [atributo*=valor], [atributo$=valor], [atributo|=valor]); y en los compuestos se encuentran los selectores agrupados, los combinadores las pseudoclases y los pseudoelementos.
las etiquetas más usadas y para qué sirven son las siguientes:

align-content:
align-items:
animation:
background:
background-color: cambia el color de fondo al color que elijas. por ejemplo: green o en valor hexadecimal #123afa o #000.
border: sirve para poner un borde alrededor del elemento
color: cambia el color de la fuente
display:
flex:
font-family:
font-size:
font-weight:
grid:
height:
hsl():
justify-content:
justify-items:
justify-self:
@keyframes:
linear-gradient():
margin:
max/ min-width:
:nth-child:
opacity():
padding:
rgb():
rgba():
text-align:
text-decoration:
text-transform:
transition:
url():
width:





