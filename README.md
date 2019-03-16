# use-webfont
A mixin for writing @font-face rules in SCSS.

# Example usage

```scss

@import 'use-webfont';


$path: '../fonts/ProximaNova/';
$prefix: 'subset-';
$formats: (woff2, woff, svg);
@include use-webfont('Proxima Nova', 400, normal, 'ProximaNova-Regular', $prefix, $path, $formats);
@include use-webfont('Proxima Nova', 400, italic, 'ProximaNova-RegularIt', $prefix, $path, $formats);
@include use-webfont('Proxima Nova', 700, normal, 'ProximaNova-Bold', $prefix, $path, $formats);
@include use-webfont('Proxima Nova', 700, italic, 'ProximaNova-BoldIt', $prefix, $path, $formats);

```

Rendered to:

```css
@font-face {
  font-family: "Proxima Nova";
  src: url("../fonts/ProximaNova/subset-ProximaNova-Regular.woff2") format("woff2"), url("../fonts/ProximaNova/subset-ProximaNova-Regular.woff") format("woff"), url("../fonts/ProximaNova/subset-ProximaNova-Regular.svg#ProximaNova-Regular") format("svg");
  font-weight: 400;
  font-style: normal; }
```
