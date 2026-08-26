# pattypan css

pattypan-css is a amalgamation of different CSS frameworks/libraries/boilerplate I've liked over the years, primarily [Skeleton](https://github.com/dhg/Skeleton) (this uses many of the same class names as Skeleton), as well as [Flexbox Grid](https://github.com/kristoferjoseph/flexboxgrid) and [Bulma](https://github.com/jgthms/bulma) to a lesser extent. I use this as a starter for my personal projects.

The name 'pattypan css' came from another old project of mine: [namurjs↗](https://www.cakehat.com/namurjs). It sounded fitting since this is supposed to be small and kinda cute.

## Fonts

Pattypan uses the operating system's sans-serif font by default and does not
make any external font requests. Projects can customize body and heading fonts
with `--font-body` and `--font-heading`.

To opt into a Google-hosted font such as Poppins, add the font links to the
project's HTML:

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link
  rel="stylesheet"
  href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap"
>
```

Then configure the font after loading Pattypan:

```css
:root {
  --font-body: "Poppins", var(--font-sans);
  --font-heading: "Poppins", var(--font-sans);
}
```

For projects that self-host their fonts, define `@font-face` rules in the
project and set the same custom properties. Include only the weights the
project uses and prefer WOFF2 files with `font-display: swap`:

```css
@font-face {
  font-family: "Poppins";
  src: url("/fonts/poppins-regular.woff2") format("woff2");
  font-style: normal;
  font-weight: 400;
  font-display: swap;
}

:root {
  --font-body: "Poppins", var(--font-sans);
}
```
