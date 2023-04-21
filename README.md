# A CHICKEN Scheme Symbol Index

## Purpose

With a browser such as `Firefox`, the `chicken-index.json` in this repository can be used as searcheable index with links to the associated documentation.
Various Scheme implementations like
[Bigloo](https://www-sop.inria.fr/mimosa/fp/Bigloo/idx.html),
[Chez Scheme](http://cisco.github.io/ChezScheme/csug9.5/csug_1.html#./),
[Gambit Scheme](http://gambitscheme.org/latest/manual/#General-index),
[Gauche](https://practical-scheme.net/gauche/man/gauche-refe/Function-and-Syntax-Index.html),
[Guile](https://www.gnu.org/software/guile/manual/html_node/Procedure-Index.html),
[MIT Scheme](https://www.gnu.org/software/mit-scheme/documentation/stable/mit-scheme-ref/Binding-Index.html),
have such an index; CHICKEN Scheme lacks this docu feature, which this `json` can provide.

## Format

The `json` is formated as a root object `"chicken_index"` with child objects of the form:
```json
{ "symbol-name (module)": "http://link.to.docu" }
```
for each symbol (A `JSON Schema` is under construction).

## Content

The `chicken-index.json` file contains symbols from the modules:

* [`scheme` module](http://wiki.call-cc.org/man/5/Module%20scheme) (R5RS procedures)
* [`(chicken scheme)` "module"](http://wiki.call-cc.org/man/5/Extensions%20to%20the%20standard) (CHICKEN's extensions)
* [`(chicken base)` module](http://wiki.call-cc.org/man/5/Module%20(chicken%20base)) (CHICKEN's standard library)
* [`(chicken module)` module](http://wiki.call-cc.org/man/5/Modules) (CHICKEN's  namespace library)

## Usage

Firefox, and likely other browsers render `.json` files in a searcheable manner.
Particularly Firefox allows filtering a json by text, and presorts an object' properties by default alphabetically with respect to the keys.

Either download `chicken-index.json` and open it locally in your (Firefox) browser,
or go to a service like: https://cdn.jsdelivr.net/gh/gramian/chicken-index/chicken-index.json
Using raw github files will not work, as the sent content type is `text/plain`,
but `application/json` is required here.
