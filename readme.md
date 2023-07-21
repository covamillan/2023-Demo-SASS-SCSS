# DEMO SASS

"ojo! si te clonas este repo recuerda,
lo primero que tenemos que hacer es:"

    `npm i`

## Instalación

1º Insertamos el comando en la terminal para instalarlo

    `npm i -d sass`

2º Creamos las carpetas css y sass

3º Añadimos el script en package.json para que identifique las carpetas y se quede watching

    `"sass":"sass sass:css --watch"`

4º Insertamos el comando que lanza el script en la terminal

    `npm run sass`

## QUÉ ES SASS

Sass (Syntactically Awesome Stylesheets) es un lenguaje de hojas de estilo que extiende CSS con funcionalidades avanzadas, como variables, mixins, herencia y anidamiento de selectores. Facilita la escritura y mantenimiento de estilos CSS al permitir una mayor reutilización de código y una sintaxis más eficiente. Sass se compila en CSS para ser utilizado por los navegadores web.

## QUÉ ES SCSS

SCSS (Sassy CSS) es una extensión de Sass que se introdujo para mejorar la sintaxis de Sass y hacerla más similar a la de CSS tradicional. SCSS permite utilizar todas las características y funcionalidades avanzadas de Sass, pero con una sintaxis que incluye llaves y puntos y comas, lo que lo hace más familiar para los desarrolladores que están acostumbrados a CSS estándar.

## QUÉ POSIBILIDADES TIENE

### VARIABLES

    Permiten almacenar valores que se pueden reutilizar a lo largo del código, facilitando el mantenimiento y la coherencia en los estilos.

### INHERITANCE

    Permite extender estilos de un selector base hacia otros selectores, evitando la duplicación de código. Evita duplicaciones de código.

### NESTING

    Permite anidar selectores dentro de otros, lo que mejora la organización y legibilidad del código.

### MIXINS

    Son bloques de estilos reutilizables que pueden contener propiedades y valores para ser incluidos en diferentes selectores.

### MODULE & PARTIALS

    Permite dividir el código en módulos independientes para facilitar el mantenimiento y la modularidad de los estilos.

### CALC

    Una función que permite realizar cálculos matemáticos en los estilos CSS, útil para establecer tamaños y dimensiones dinámicas.
