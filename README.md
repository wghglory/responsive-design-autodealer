# Responsive Design Auto Dealer

Responsive design, media query, scss, koala

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
