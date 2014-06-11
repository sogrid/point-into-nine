##☞9

###pin
Layout configuration with the following parameters:

1. area to accompy
2. point of interest
3. slice orientation
4. element alignments eg. $selector: $orient-slice:1-9 $align-contents: 1-9

```css
figure:nth-of-type(1) {
  @include pin(100% 50vmin, 52% 25%, row, ('> nav': 4 5, '> figcaption': 6 4));
}
```
###pin--debug

This draws a crosshair over your point of interest, fades back the pin image, highlights slices, and adds 1em grid lines over the whole container.
```css
figure:nth-of-type(1) {
  @include pin--debug(52% 25%);
}
```

###pin_image

Defines a image to be aligned to the point of interest.

```css
figure:nth-of-type(1) {
  @include pin_image(url('//path/to/image.png'));
}
```

###pin_image--uncover

Pin images, by default, are absolutely positioned and covering all the available space within the defined area. This puts the image in a relatively positioned context at a natural or proportionally-scaled size.

```css
figure:nth-of-type(1) {
  @media only screen and (max-width: 40em) {
    @include pin_image--uncover;
  }
}
```
