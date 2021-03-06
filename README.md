# Pla de Govern

[El cuadro de mando del Pla de Govern del Ayuntamiento de Castelló](http://www.castello.es/frontal/plagovern/pages/estat.php) se utiliza para ver el grado de avance en el cumplimiento del plan de gobierno del Ayuntamiento de Castelló. Los datos para el cuadro de mando vienen del [tablero _Trello_](https://trello.com/b/gffJXegr/pla-de-govern-ajuntament-de-castello-de-la-plana) donde se gestiona el cumplimiento de los compromisos.

## Instalación

Añade la siguiente propiedad `require` en tu fichero `composer.json`:

`"ajuntamentdecastello/pladegovern"`

y luego ejecuta:

`$ composer install`

Si no quieres usar _composer_, indica en la cabecera de tu fichero php:

`require_once 'src/AjuntamentDeCastello/Kanban/CastelloKanbanBoard.php';`

## Código fuente y ejemplos

La clase _CastelloKanbanBoard_ (`src/AjuntamentDeCastello/Kanban/`) recupera la información del tablero _Trello_ y calcula los indicadores a partir de esa información. Debes indicar, en las llamadas al constructor de la clase _CastelloKanbanBoard_, tus propios datos para el acceso a la API de _Trello_ (`key` y `application token`)

El _cuadro de mando ejemplo_ (`examples/index.php`) hace uso de un código javascript para generar el gráfico de donuts (`examples/js/donut-multiples.js`) y de un código php para generar los datos para ese gráfico de donuts en formato CSV (`examples/data.csv.php`).

Estos códigos del _cuadro de mando ejemplo_ hacen uso, además de la clase _CastelloKanbanBoard_, de los siguientes componentes:
* [Bootstrap](https://getbootstrap.com/): Biblioteca para generar páginas web responsivas. Liberada bajo licencia MIT. Copyright &copy; 2011-2018 Autores de Bootstrap y Twitter, Inc. 
* [D3.js](https://d3js.org/): Biblioteca de JavaScript para producir visualizaciones de datos. Liberada bajo licencia BSD. Copyright &copy; 2017 Mike Bostock. Es necesario utilizar la versión 3.
* [Font Awesome](https://fontawesome.com/): Conjunto de herramientas de fuentes e iconos. Liberadas bajo las licencias CC BY (iconos), SIL OFL (fuentes) y MIT (código). Copyright &copy; 2018 Autores de Font Awesome y Fonticons, Inc.
* [Spin JS](https://spin.js.org/): Biblioteca para generar el spinner de "cargando". Liberada bajo licencia MIT. Copyright &copy; 2011-2018 Felix Gnass.

Por simplicidad, estas bibliotecas se incorporan al _cuadro de mando ejemplo_ mediante enlace a Content Delivery Networks (CDNs). Para despliegues en producción recomendamos que descargues las librerías en tu propio servidor, en lugar de usar CDNs, por las implicaciones con el Reglamento Europeo de Protección de Datos de la carga de estas librerías desde CDNs.

## Para más información

* [Ayuntamiento de Castelló - Pla de Govern - Programa de Gobierno Municipal](http://pladegovern.castello.es)
* [Ayuntamiento de Castelló - Pla de Govern - Tablero Trello](https://trello.com/b/gffJXegr/pla-de-govern-ajuntament-de-castello-de-la-plana)
* [Ayuntamiento de Castelló - Pla de Govern - Trello: ¿Qué es y por qué lo usamos?](http://www.castello.es/frontal/plagovern/pages/trello_what_is.php)

## Licencia

Copyright &copy; 2016-2018 Ayuntamiento de Castelló (Castellón, Spain).
 
Este trabajo está licenciado bajo [European Union Public Licence (EUPL)](https://joinup.ec.europa.eu/collection/eupl/eupl-guidelines-faq-infographics).

Ver fichero LICENSE para información adicional.
