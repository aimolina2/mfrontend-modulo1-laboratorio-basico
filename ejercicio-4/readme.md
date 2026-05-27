# Laboratorio Layout BASICO. Ejercicio 4.

Aplicamos grid para crear la card asegurando que los bloques que la conforman se apilan en columna y ocupan el espacio correspondiente.

Lo aplicamos primero en la card e indicamos el gap para separar los elementos principales: imagen de contenido de la card.

En el contenido volvemos a usar `display: grid` para conseguir una estructura de bloques que definimos con `grid-template-areas:
    "title"
    "text"
    "date"
    "button";`
