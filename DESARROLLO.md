# Desarrollo

Algunos detalles sobre remark.js, MathJax, etc.

## remark.js

El sitio esta basado sobre [remark.js](https://github.com/gnab/remark).

Observaciones:

 * Solo se puede imprimir, o exportar en PDF, correctamente en Chrome/Chromium - Ver https://github.com/gnab/remark/issues/164

## MathJax

Para incluir las formulas matemáticas, se utiliza sintaxis [LaTeX](https://en.wikibooks.org/w/index.php?title=LaTeX/Mathematics), y la librería [MathJax](http://www.mathjax.org/).

## Sitio

Para permitir la visualización del sitio sin conexión a Internet, se agregaron las siguientes librerías en local en este repositorio:

 * [remark.js](https://github.com/gnab/remark) - se descargó y compiló en local, y se copió el archivo `js/remark.min.js`.
 * [MathJax](http://www.mathjax.org/) - mediante un submodule git.
