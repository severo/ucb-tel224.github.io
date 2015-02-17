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

## Figuras

Para recuperar las figuras del PDF de Oppenheimer:

1. descifrar el PDF

```
sudo aptitude install qpdf
qpdf --decrypt Oppenheim\,\ Schafer\ -\ Tratamiento\ de\ señales\ en\ tiempo\ discreto\,\ 3ra\ ED.pdf libro.pdf
```

2. convertir todas las páginas en SVG de una vez (al final verificamos cuantas páginas fueron extraídas)

```
sudo aptitude install pdf2svg
mkdir libro
pdf2svg libro.pdf libro/libro-p%d.svg all
ls -1 libro | wc -l
```

3. Para extraer la figura de la página 77, 

  * abrir en Inkscape con `inkscape libro/libro-p77.svg`,
  * desagrupar la página con `Ctrl+A, Ctrl+U`,
  * seleccionar la figura,
  * invertir la selección, con `!`,
  * borrar, con `Suppr`,
  * ajustar el tamaño del lienzo a la página, con `Ctrl + Shift + D` y presionando "Ajustar página a dibujo o selección"
  * guardar como SVG, con `Ctrl + Maj + s`
  * cerrar Inkscape con `Ctrl + Q`
