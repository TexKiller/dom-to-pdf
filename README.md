# dom-to-pdf

dom-to-pdf generates a printable PDF from DOM node using HTML5 canvas and svg.

## Install

```
npm i atomics-dom-to-pdf
```

## Usage
```javascript
var domToPdf = require('dom-to-pdf');

var element = document.getElementById('test');
var options = {
  filename: 'test.pdf'
};
domToPdf(element, options, function(pdf) {
  console.log('done');
});
```

## Options
* `filename` - string, name of resulted PDF file, default name is `generated.pdf`
* `excludeClassNames` - array of strings, list of class names of elements to exclude from PDF, e.g. `['Loading', 'ExcludeMeFromPdf']`
* `excludeTagNames` - array of strings, list of html tags to exclude from PDF, e.g. `['button', 'input', 'select']`
* `overrideWidth` - number, overrides a width of a container DOM element 
* `proxyUrl` - string, e.g. `/api/proxyImage?url=`, a route in your app which renders images on your domain in order to avoid problems with CORS with the images on a DOM
* `compression` - string, compression of the generated image, can have the values 'NONE', 'FAST', 'MEDIUM' and 'SLOW'. (default is 'NONE')
* `scale` - number, increases an image's size before exporting to improve the image quality
*`download` - option to download pdf or simply just return pdf without downloading


## MIT License
Copyright (c) 2022 Osman Mazinov

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.

