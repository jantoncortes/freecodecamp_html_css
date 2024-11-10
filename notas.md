# NOTAS DEL CURSO
https://www.youtube.com/watch?v=XqFR2lqBYPs

JS aplica funcionalidades a la web, la hace interactiva

##Título secundario

* Lista
* Lista

**Negritas** *Cursiva* 

# Código, ponemos 3 tildes arriba y abajo y el lenguaje que usamos

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <link href="style.css" rel="stylesheet">
  </head>
  <body>
    <div class="pinguino">
      <div class="pinguino-inferior">
        <div class="mano-derecha"></div>
        <div class="mano-izquierda"></div>
        <div class="pie-derecho"></div>
        <div class="pie-izquierdo"></div>
      </div>
    </div>
  </body>
</html>

``` 

<img> No necesita una etiqueta de cierre
<main></main> contenido principal de la web. Contenido único de la web, no ser repite y no debe ser parte de otro elemento.
en una etiqueta <a> rel="noopener noreferrer" evita el ataque tabnabbing.

enlaces internos: <a href="#parrafo-1">Parrafo 1</a> me lleva al párrafo 1 que tiene precisamente ese id. 
enlaces muertos: <a href="#"> se utilizan para dejar el código para más adelante indicar la dirección de destino.
<strong> para negrita
<em> para cursiva
<s> para tachar (strickthrough)
<hr> línea horizontal (horizontal ruel)
<form> formularios
    <form action="/enviar-respuesta">
      <input type="text">
      <button type="submit">Enviar</button>
    </form>

checked se añade al input no al label


# ATAJOS
ALT+Z el código se adapta al tamaño de la ventana
CTRL + ç convierte o desconvierte en comentario

mdn web docs: red de desarrolladores de mozilla.  
https://developer.mozilla.org/es/ y en la búsqueda vamos preguntando por el tema que nos interese.


# CSS
3 Estilos posibles:
- EStilos en línea, se añade directamente a la etiqueta de apertura del elemento en el archivo HTML
- <style></style>: se añade ese elemento en el <head> del archvivo HTML
- Archivo.css. Los dos archivos se conectarán a través de  <link href="style.css" reL="stylesheet"> dentro de head

    selectores de tipo h2{}
    selectores de clase .class name{}

Google fonts:https://fonts.google.com/ y copiamos el o los links en el <head> del HTML.

## Imágenes:
img {
  width: 200px;
  border-width: 5px;
  border-color:blue;
  border-style: solid dashed dotted;
}
Podemos crear clases para que no afecte en este caso a todas las imágenes, si no a las que tengan la clase que determinemos.
Ver todas la variedades de bordes.
Las combinaciones se asignan en el sentido de las agujas del reloj.

.bordes-redondeados{
  border-radius: 20px;
}
50% sería un círculo casi perfecto si partimos de un cuadrado.

Color de fondo de un <div>:
div {
  background-color: beige;
}

Atributo id en CSS:

/* Asignar estilo a un id, se precede de # */
#titulo-principal {
  font-size: 30px;
  font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
  color: green;
}
Los id también servirán en JS para asignar características específicas.

## Controlar el espacio de los elementos:
Padding, distancia entre el contenido de un elemento html y su borde.
Se puede asignar distinto padding para cada uno de los lados del elemento.
img {
  padding: 35px 15px 10px 5px; esta es la forma abreviada de lo de abajo
  /* padding-top: 35px;
  padding-right: 15px;
  padding-left: 10px;
  padding-bottom: 5px; */
  background-color: yellow;
  border-width: 2px;
  border-color:black;
  border-style: solid;
}

Margin: distancia entre el borde de un elemento y el borde de otro elemento.

Padding vs margin:


Selectores de atributo.
En este ejemplo, todas las imágenes con el atributo alt*/
img[alt]{
  border-radius: 50%;
}

/* ahora, los elementos type=radio */
[type="radio"]{
  margin: 50px;
}


a[href="https://www.freecodecamp.org/espanol/"]{
  color:green;
  text-decoration: none;
  font-weight: bold;
  font-size:x-large
}

## Unidades absolutas y relativas
ver ejemplo ya hecho.
https://developer.mozilla.org/es/docs/Learn/CSS/Building_blocks/Values_and_units


La última clase en CSS es la que va a tener prioridad, el último valor asignado es el que prevalece. En HTML da igual el orden de las clases dentro de un mismo elemento.

En CSS  una clase sí tiene prioridad sobre su elemento genérico. Y un id tiene prioridad sobre una clase.

Si el estilo está en línea en HTML, la prioridad es la de este y no la que le da el CSS. A menos que pongamos en CSS !important.
.texto-azul {
    color: blue !important;
}

colour picker: para ver los códigos hexadecimales de los colores.
https://imagecolorpicker.com/color-code/2596be

Los códigos de 6 se pueden abreviar, cuando están repetidos en cada parte, p.e.
#000000 se abreviaría como #000
#00ff00 se abreviaría como #0f0
también pueden ir en mayúsculas.

rgb (0, 255, 255) es igual que el #0ff. Un tercer elemento entre 0 y 1 daría el grado de transparencia del color.
p.e. rgba (0, 255, 255, 0.4)


## Variables CSS (ejercicio pingüino)

--pinguino-barriga: es una variable css. Se define para poder reusarla a lo largo del documento, y tener que actualizar solo esa variable para que actualice el resto donde se actualiza.
Se ponen valores de respaldo para las variables por si no son reconocidas por el navegador.
.mejilla-derecha {
  top: 15%;
  left: 35%;
  background: var(--pinguino-barriga, white);
}

Valor de respaldo para cuando un navegador no reconoce las variables, se pone antes del valor de la variable, y no a continuación de la misma como hemos hecho antes. Pero mejor mantener también ese valor de segundo respaldo por si tenemos errores de escritura.
.pie-derecho {
  top: 85%;
  left: 60%;
  background: orange;
  background: var(--pinguino-pico);
}

Para poder usar la variable css en todo el documento:

:root {
    --pinguino-barrigo: pink;
}

al estar en root, ya reconocerá la variable en el body, prevaleciendo en este caso el color pink.

body {
    background: var(--pinguino-barriga, red);
}

Cambiar variable para un área específica:











