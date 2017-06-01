# Gentle-TDD
## Inicializar nmp

```sh
$ npm init
```
## Agregando Datos
```js
  {
    "name": "gentle-tdd",
    "version": "1.0.0",
    "description": "Ejercicio de TDD",
    "main": "index.js",
    "scripts": {
      "test": "test"
    },
    "repository": {
      "type": "git",
      "url": "git+https://github.com/FlorTello/gentle-example.git"
    },
    "keywords": [
      "test",
      "tdd",
      "ejemplo"
    ],
    "author": "FlorTello",
    "license": "ISC",
    "bugs": {
      "url": "https://github.com/FlorTello/gentle-example/issues"
    },
    "homepage": "https://github.com/FlorTello/gentle-example#readme"
  }
```
## Agegando Archivos
 * Agregando .gitignore: agregando el siguiente contenido : /node_modules/*
```sh
vi .gitignore
```
 * Agregando archivos:
    flickr-fetcher.js para el módulo que recoge los datos y lo transforma;
    photo-lister.js para el módulo que toma la lista, lo convierte a HTML y lo añade a la página;
    flickr-fetcher-spec.jspara el código de prueba flickr-fetcher.js; y
    photo-lister-spec.jspara el código para probar photo-lister.js.
    
 ## Escribiendo pruebas
```js
// flickr-fetcher-spec.js
'use strict';
var expect = require('chai').expect;

describe('FlickrFetcher', function() {
    it('should exist', function() {
        var FlickrFetcher = require('./flickr-fetcher.js');
        expect(FlickrFetcher).to.not.be.undefined;
    });
});
```
 * Por lo tanto, vamos a ejecutar la prueba:
 ```sh
  mocha --reporter=nyan flickr-fetcher-spec.js
 ```
```

