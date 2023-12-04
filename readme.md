# DOMBuilder

`DOMBuilder` is a JavaScript utility class for building and manipulating HTML elements. It provides a convenient and chainable interface for creating, configuring, and appending HTML elements.

## Table of Contents

- [Usage](#usage)
  - [Creating an Instance](#creating-an-instance)
  - [Creating Elements](#creating-elements)
  - [Setting Attributes](#setting-attributes)
  - [Adding Classes](#adding-classes)
  - [Setting ID and Title](#setting-id-and-title)
  - [Appending Elements](#appending-elements)
  - [Setting Image Source](#setting-image-source)
  - [Attaching Event Listeners](#attaching-event-listeners)
  - [Converting from HTML String](#converting-from-html-string)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)

## Usage

### Creating an Instance

```javascript
const builder = new DOMBuilder();
```

### Creating Elements
```javascript
const myDiv = builder.create('div', 'Hello, DOMBuilder!');

### Setting Attributes
```javascript
const builder = new DOMBuilder();
```

### Adding Classes
```javascript
myDiv.class('my-div');
// or
myDiv.classes(['class1', 'class2']);

```
### Setting ID and Title
```javascript
myDiv.id('uniqueId');
myDiv.title('This is a div');
```

### Appending Elements
```javascript
const parentElement = document.getElementById('parent-container');
myDiv.appendTo(parentElement);
```

### Setting Image Source
```javascript
const myImage = builder.create('img').setSrc('path/to/image.jpg');

```

### Attaching Event Listeners
```javascript
myDiv.event('click', () => {
  console.log('Div clicked!');
});

```

### Converting from HTML String
```javascript
const htmlString = '<div class="html-div">Hello from HTML!</div>';
const htmlElement = DOMBuilder.fromHTML(htmlString).getElement();

```

## Examples
Creating a button and attaching a click event:
```javascript
const builder = new DOMBuilder();
const myButton = builder.create('button', 'Click me')
  .class('my-button')
  .appendTo(document.body)
  .event('click', () => {
    alert('Button clicked!');
  });
```

