# LEARNING SASS

"ojo! si te clonas este repo recuerda,
lo primero que tenemos que hacer es:"
`npm i`

"
sass es un metalenguaje de programación, que permite escribir hojas de estilo con las características propias de un lenguaje de programación, funciona como un compilador, es decir, lo que escribimos en sass lo "traduce" a lenguaje css, permitiendo utilizar:"

###### INHERITANCE/EXTEND

###### VARIABLES

###### NESTING

###### PARTIAL

###### MODULES

###### MIXINS

###### CALC

## Ventajas respecto al css:

    	- Reduce el tiempo para crear y mantener el CSS
    	- Permite tener una organización modular de los estilos
    	- Proporciona estructuras avanzadas propias de los lenguajes de programación, como variables, funciones, etc.
    	- Permite vigilar los ficheros, de tal manera que, si ha habido un cambio en la hoja de estilos.
    	- Se regenera automáticamente (modo watch).
    	- Existen muchas herramientas asociadas, muchas librerías hechas con Sass y una comunidad muy importante de usuarios.

## Desventajas:

    	- Hay que aprender a utilizar una nueva herramienta
    	- Hay un tiempo de consumo en el proceso de generación o compilación del CSS (mínimo)

## Instalación

    1º Insertamos el comando en la terminal

`npm i -d sass`

    2º Instalamos extensión de sass
    3º Creamos las carpetas css y sass
    4º Añadimos el script en package.json para que identifique las carpetas y se quede watching

`"sass":"sass sass:css --watch"`

    5º Insertamos el comando que lanza el script en la terminal

`npm run sass`

## VARIABLES

    - $
    Podemos hacer que se guarden variables simplemente poniendo el simbolo de dollar delante.

    ejemplo:

                $primary-color: #333;

                .title1{
                  color: $primary-color;
                  display:flex;
                  justify-content:center;
                }
                .secondary-title{
                  color: $primary-color;
                  font-size:2rem;
                  padding:1rem;
                  font-family:verdana;
                }
                .footer{
                  color: $primary-color;
                }

## INHERITANCE

    - @EXTEND
      Podemos hacer que se herede como en los lenguajes de programación, utilizando el @extend y el %

      1º con el porcentage indicamos las características que queremos que se herede
      2º lo llamamos con @extend en donde queremos que se apliquen

      ejemplo:

                %paragraph-base {
                border: 1px solid #ccc;
                  padding: 10px;
                  color: #333;
                }

                .paragraph1 {
                  @extend %paragraph-base;
                    text-decoration: underline;
                }
                .paragraph2 {
                  @extend %paragraph-base;
                    text-decoration: overline;
                }

## NESTING

    - anidación
      podemos hacer que se aniden uno dentro de otro, ahorrándonos bastante código.

      ejemplo:

      si queremos dar algun formato SOLO al titulo del primer article o a un span que
      esta dentro del parrafo del artículo-1

          .article1{
            .secondary-title{
              font-weight: bold;
            }
            .paragraph1{
              span{
                text-transform: uppercase;
              }
            }
          }

## MIXINS

    - funciones
      Podemos hacer que se guarden diferentes características en un mixin y hacerlo variar al llamarlas
      con @include

      ejemplo:

      @mixin functionName ($variableName: #7092BE, $variable2Name: #3F48CC){
        text-transform: uppercase;
        border: 1px solid $variableName;
        background: $variable2Name
      }

      .paragraph2{
        @include functionName()
      }
      .paragraph3{
        @include functionName($variable2Name: lightgoldenrodyellow)
      }

## MODULE & PARTIALS

        - _ y @use
        Podemos hacer que nuestro código sass se reparta en varios ficheros utilizando el _ para el nombre del
        fichero y luego llamándolo en el fichero principal con el @use

        ejemplo:

        _nombreDelFichero.scss

            metemos por ejemplo las mixins que hemos hecho antes en este fichero

                    @mixin functionName ($variableName: #7092BE, $variable2Name: #3F48CC){
                      text-transform: uppercase;
                      border: 1px solid $variableName;
                      background: $variable2Name
                    }
                    .paragraph2{
                      @include functionName()
                    }
                    .paragraph3{
                      @include functionName($variable2Name: lightgoldenrodyellow)
                    }

        style.scss

            en el fichero principal, recomendablemente al principio, llamamos al módulo con el @use

            @use 'nombreDelFichero';

## CALC

      - "+, -, *, /"

      podemos utilizar operaciones matematicas

      section{
                widht: 400px + 100px
                }
