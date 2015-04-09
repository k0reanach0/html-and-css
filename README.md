# html-and-css
HTML and CSS Helpful Stuff

#### Famous Box Model
```css
html {
  box-sizing: border-box;
}

*, *:before, *:after {
  box-sizing: inherit;
}
```

#### Font Sizing
However, I have found this method quite limiting in terms of ability to scale. Although my font sizing looks good on medium and small screens, it could be better optimised for larger ones. Even if users have the option to zoom in, that isn’t something we want them to need to do.

My solution is therefore to work with rem (using pixels as a fallback).

```css
html {
  font-size: 62.5%; /* sets the base font to 10px for easier math */
}

body {
  font-size: 16px;
  font-size: 1.6rem;  
  /* sets the default sizing to make sure nothing is actually 10px */
}

h1 {
  font-size: 32px;
  font-size: 3.2rem;
}
```

This allows me to scale up my font sizes simply by writing -

```css
@media screen and (min-width: 1280px) {
  html {
    font-size: 100%;
  }
}
```
