# palettes.less

A grid-only LESS stylesheet. Lays out HTML elements on a [http://en.wikipedia.org/wiki/Grid_(graphic_design)](typographic grid).

## Installing

### Installing the .less version
1. Clone the repository
1. Copy 'gridit.less' to your project's less directory
1. Add an @import "gridit.less"; to a suitable place in your .less file
1. Use the provided .row# and .cell# classes on your grid rows and columns

### Installing the .css version
For now, there is no precompiled .css. If you need one, drop us a line and we'll precompile one for you.

Later if we get enough of these kinds of requests we might automate the precompile.

## Example

```LESS
@import 'reset.css';
@import '../grid.less';

body { background: lighten(cyan, 77%); }
```

```HTML
<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet/less" type="text/css" href="style.less"></link>
  <script src="//cdnjs.cloudflare.com/ajax/libs/less.js/1.3.3/less.min.js" type="text/javascript"></script>
</head>

<body>
  <div class="row1">
    <span class="cell4">This cell occupies four grid boxes horizontally</span>
    <span class="cell3">And this one three</span>
  </div>
</body>
</html>
```

## Usage

### Rows

Use rows to create rows of grids. They work more or less like the <tr> tag in HTML.
  
### Cells

Use rows to create columns of grids. They work more or less like the <td> tag in HTML.

### Configuring

TODO

### Nested grids

If you want to achieve something similar to the <td> tag's "colspan", you can nest the rows and nodes. So if you for example want
to have a 3x3 area for an image on the left and a group of 1x1 action buttons for it on it's right, you should do it more or less like this:

```HTML
<div class="row3">
  <span class="cell3">
    <img ...>
  </span>
  <div class="cell2">
    <div class="row1">
      <span class="cell1">Button 1</span>
      <span class="cell1">Button 2</span>
    </div>
    <div class="row1">
      <span class="cell1">Button 4</span>
      <span class="cell1">Button 5</span>
    </div>
  </div>
</div>
```

# License

The library is licensed under the MIT-license:

> Copyright (C) 2012 Aphex Consulting Oy

> Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

> The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

> THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.