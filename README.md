# QR Generator

Generador de códigos QR en node.js en fichero .svg. Se implementan dos variantes:

  - Genera QR y guarda en un fichero /codigos/quewy.svg
  - Muestra el código en el navegador en localhost:3000

### Version
1.0.0

### Dependencias
* qr-image :  ^3.1.0
* express: ^4.11.2 (Solo para publicar en web)

### Instalación
Necesitas tener instalado node.js. Puedes descargarlo desde www.nodejs.org.
Una vez instalado, clona el repositorio a una carpeta:

```sh
$ git clone https://github.com/ivanbtrujillo/QRGenerator-NodeJS Qr-Generator
$ cd Qr-Generator
$ npm install
```

### Ejecución
```sh
npm start
```

### Cómo funciona
En el fichero index.js vienen las dos versiones (fichero y navegador). Cuando se ejecuta el servidor se genera un QR y se vuelga a un fichero .svg en la carpeta codigos. Posteriormente genera otro QR distinto y lo muestra en el browser en el browser.

### Salida a fichero
Genera un fichero .svg en la carpeta códigos. 

### Salida a localhost
Publica una web en localhost con el codigo QR. Localhost:3000

### Cambio de carpeta de salida
Modificar la salida en la variable output:
var output = fs.createWriteStream('codigos/quewy.svg')

### Cambio de la string que queremos generar con el QR
Modificar la string en la variable code:
var code = qr.image('String a generar', { type: 'svg' });  

## Copyright & License

The MIT License (MIT)

Copyright (c) 2015 Ivanbtrujillo

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
