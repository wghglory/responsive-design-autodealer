# Responsive Design Auto Dealer

Responsive design, media query, scss, koala

## Limit main. nav/header/footer stretch but text moves to center

Limit width and extend background by wrapper:

![Wrapper usage](http://om1o84p1p.bkt.clouddn.com/1529848332.png?imageMogr2/thumbnail/!70p)

---

**Limit all:**

![Limited width](http://om1o84p1p.bkt.clouddn.com/1529845907.png?imageMogr2/thumbnail/!70p)

```scss
// _large.scss
header,
nav,
main,
footer {
  max-width: 60rem;
  margin: 0 auto;
}

// if wanna space on the header and bottom
body {
  padding: 1rem 0;
}
```

**Limit only main and nav, but not header or footer:**

![Limited only main and nav, but not header or footer](http://om1o84p1p.bkt.clouddn.com/1529846062.png?imageMogr2/thumbnail/!70p)

```scss
// _large.scss
nav,
main {
  max-width: 60rem;
  margin: 0 auto;
}
```

## Koala

**Koala specifies that the output points to css/styles.css**.

## Start up project

vscode liver server + koala to compile scss.

## import order

1.  CSS reset/Normalize
1.  Small screen rules (default, major code)
1.  Medium screen rules (overwrite default)
1.  Large screen rules (overwrite default and medium especially!)

## 3 ways

### Way 1

Small.css:

```scss
@media screen and (min-width: 320px) and (max-width: 500px) {
}
```

Medium.css:

```scss
@media screen and (min-width: 501px) and (max-width: 960px) {
}
```

Large.css:

```scss
@media screen and (min-width: 961px) and (max-width: 1600px) {
}
```

### Way 2

Small.css:

```scss
@media screen and (max-width: 500px) {
}
```

Medium.css:

```scss
@media screen and (min-width: 501px) and (max-width: 960px) {
}
```

Large.css:

```scss
@media screen and (min-width: 961px) {
}
```

### Way 3 (Used Frequently)

Small.css: No rules, default!

Medium.css:

```scss
@media screen and (min-width: 500px) {
}
```

Large.css:

```scss
@media screen and (min-width: 1140px) {
}
```
