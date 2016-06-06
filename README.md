### SVG for icons

```css
.element {
  background: url("icon.svg");
}
```

### Equal Width Table Cells

```css
.cell {
  table-layout: fixed;
}
```

### Equal spacing between elements

```css
.list {
  display: flex;
  justify-content: space-between;
}

.list__item {
  flex-basis: 25%;
}
```

### Preserve Ratio

```css
.container {
  height: 0;
  position: relative;
  padding-bottom: 30%;
}

.container div {
  height: 100%;
  left: 0;
  position: absolute;
  top: 0;
  width: 100%;
}
```

### Style broken images

```css
img {
  display: block;
  font-family: Arial;
  font-weight: 300;
  height: auto;
  line-height: 2;
  position: relative;
  text-align: center;
  width: 100%;
}

img:before {
  content: "Missing Image";
  display: block;
  margin-bottom: 10px;
}

img:after {
  content: "(url: " attr(src) ")";
  display: block;
  font-size: 12px;
}
```

### Use CSS content to separate lists - [CodePen](http://codepen.io/eeyore/pen/BzoyGG "View CodePen") 
```css
ul > li:not(:last-child)::after {
  content: ",";
}
```

### Use `:not` to remove styles
```css
.list li:not(:last-child) {
  border-right: 1px solid #000;
}
```

### Easy global font sizing with rem

```css
html {
  font-size: 16px;
}

h1 {
  font-size: 2em;
}

p {
  font-size: 1em;
}

.component {
  font-size: 1.25rem;
}
```

### Flexible Type

Allow fonts to adjust with each viewport.

```css
:root {
  font-size: calc(1vw + 1vh + .5vmin);
}

body {
  font: 1em/1.6 sans-serif;
}
```
