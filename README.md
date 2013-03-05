# Media Shortcuts

> Sass media queries shortcuts

A bundle of differents Sass media-queries shortcuts.

![Fonzie approved](https://dl.dropbox.com/u/14108185/Pictures/fonzie.jpg)

## Installation

```
fonzie install media-shortcuts
```

## Usage

```scss
@import "media-shortcuts";
```

```scss
selector {
    @include media-min-width(320px) {
        @include landscape {
            // your content
        }
    }

    @include media-min-height(480px) {
        // some other rules
    }
}
```

## Availables shortcuts

### Screen size min & max (for width & height)

+ `media-min($min-size, $prop: 'width')`
+ `media-max($min-size, $prop: 'width')`
+ `media-gap($min-size, $max-size, $prop: 'width')`

+ `media-min-width($min-width)`
+ `media-max-width($max-width)`
+ `media-gap-width($min-width, $max-width)`

+ `media-min-height($min-height)`
+ `media-max-height($max-height)`
+ `media-gap-height($min-height, $max-height)`

### Orientation (portrait/horizontal & landscape/vertical)

+ `media-portrait`
+ `media-landscape`

### Resolution screen (hidpi, "retina" display)

```scss
$media-screen-default-dpi: 96 !default;
$media-pixel-ratio-breakpoint: 1.5 !default;
```

+ `media-resolution($ratio: $media-pixel-ratio-breakpoint, $minOrMax: 'min')`
+ `media-pixel-ratio($ratio: $media-pixel-ratio-breakpoint, $minOrMax: 'min')`
+ `media-highres($ratio: $media-pixel-ratio-breakpoint) (shortcut for pixel-ratio)`

### Available for you JavaScripts

+ `media-queries-for-js($name, $media-queries)`

```js
var size = window.getComputedStyle(document.body,':after').getPropertyValue('content');
if (size == 'widescreen') {
    // code for 'widescreen' !
}
```

## License

Copyright (c) 2012 Maxime Thirouin

Released under [MIT Licence](http://moox.mit-license.org/)

