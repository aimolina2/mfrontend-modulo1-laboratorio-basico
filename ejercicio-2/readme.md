# Laboratorio Layout BASICO. Ejercicio 2.

Para poder tener dos temas diferentes y variar así el estilo de nuestra página (index.html) creamos contamos con una página común donde recogemos la estructura principal. Esta hoja de estilos (mystyle.scss) es la que tenemos linkada en el html.

Contamos con otras dos hojas de estilo, una por cada tema, que recogen las variaciones. Usando Sass definimos las variables de color, fuente, border radius y sombreado.

- styleA.scss: usa tonos azules, y otras caracerísticas.
- styleB.scss: tonos verdes y otras diferencias.

Para alternar entre los temas solo tenemos que cambiar la hoja a importar en mystyle.scss.
El tema que no usamos aparece de forma comentada para que no se aplique.

```
@import "styleA";
// @import "styleB";
```
