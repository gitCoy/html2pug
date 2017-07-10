# html2pug
Converts **HTML** to **Pug** templating language (formerly Jade)

Turns this :unamused:
```html
<!doctype html>
<html lang="en">
  <head>
    <title>Hello World!</title>
  </head>
  <body>
    <div id="content">
      <h1 class="title">Hello World!</h1>
    </header>
  </body>
</html>
```

Into this :tada:
```pug
!doctype html
html(lang='en')
  head
    title Hello World!
   body
    #content
      h1.title Hello World!
```

## Install

Get it on [npm](https://www.npmjs.com/package/html2pug):

```bash
npm i -g html2pug
```

## Usage

### CLI
Accept input from a file and write to stdout:

```bash
html2pug < example.html
```

Or write to a file:
```bash
html2pug < example.html > example.pug
```

### Programmatically

```js
const html2pug = require('html2pug')

const html = '<header><h1 class="title">Hello World!</h1></header>'

// Inside an async/await function
const pug = await html2pug(html, { tabs: true })
```

### Options

Name | Type | Default | Description
--- | --- | --- | ---
tabs | Boolean | `false` | Use tabs instead of spaces
