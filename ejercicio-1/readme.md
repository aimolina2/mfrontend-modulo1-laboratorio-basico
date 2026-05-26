# Laboratorio Layout BASICO. Ejercicio 1.

Paleta de colores dinamica donde el brillo baja gradualmente. En el centro encontramos el color base, y se orcurece bajando el brillo conforme va hacia la izquierda y se hace más brillante hacia la derecha.

Usamos Sass.

Definimos los colores principales que que vamos a usar tanto en las cajas como para el color de fuente.

```
$color-base-1: rgb(143, 231, 196);
$color-base-2: rgb(108, 163, 240);
$color-base-3: rgb(161, 130, 201);
$color-font: rgb(47, 54, 148);
```

Mediante bucles aplicamos los colores dependiendo del número de contenedor. Del 1 al 3, si tu índice es = 1 se aplica un color, si es = 2 otro y si es = 3 otro.

E igual para dar más brillo u oscuridad al color.

- Por un lado hablamos de la clase darken, que irá del 1 al 4 (hacia la izquierda) restando luz al color base (oscurece) y sumando luz al color de la fuente.

```
@for $d from 1 through 4 {
    .container-#{$i} > .darken-#{$d} {
      background-color: color.adjust($color, $lightness: -$d * 5%);
      color: color.adjust($color-font, $lightness: $d * 20%);
    }
  }
```

- Por por otro, la clase lightness, del 1 al 4 pero hacia la derecha, que suma luz al color base y resta al color de fuente hasta convertirse en un color muy oscuro casi negro.

```
@for $l from 1 through 4 {
    .container-#{$i} > .lighten-#{$l} {
      background-color: color.adjust($color, $lightness: $l * 5%);
      color: color.adjust($color-font, $lightness: -$l * 10%);
    }
  }
```
