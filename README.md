# SASS Base by Luis Melo

This code base is intended to be used as a basis for your project, using SASS.

# Table of Contents

1. [Installation](#installation)
2. [Import to your SASS project](#import-to-your-sass-project)
3. [API](#api)
   * [Mixins](#mixins)
   * [Classes](#classes)
   * [Functions](#functions)
4. [Contributing](#contributing)
5. [License](#license)

# Installation

```npm install sass-base-lm --save-dev``` 

or 

```yarn add sass-base-lm --dev```

# Import to your SASS project

In your SASS root file, just import the `styles.scss`:
```
//  Without Webpack
@import 'node_modules/sass-base-lm/assets/styles';

//  With Webpack
@import '~/node_modules/sass-base-lm/assets/styles';
```

# API

## Mixins
### media(dimension: **string**)

Allows to create styles to be used in intervals of screen widths. The `dimension` argument can be:
* `screen`: Only apply styles when using a computer screen, tablet, smart-phone, etc.
* `landscape`: Only apply styles when using a screen and landscape orientation.
* `portrait`: Only apply styles when using a screen and portrait orientation.
* `xsmall-up`: Apply when width is greater than 0em.
* `xsmall-only`: Apply when width is up to 48em.
* `small-up`:  Apply when width is greater than 48em.
* `small-down`:  Apply when width is up to 62em.
* `small-only`:  Apply when width is between 48em and 62em.
* `medium-up`:  Apply when width is greater than 62em.
* `medium-down`:  Apply when width is up to 75em.
* `medium-only`:  Apply when width is between 62em and 75em.
* `large-up`:  Apply when width is greater than 75em.

### media-query(dimension: **string**)

Create a media query where the max-width will be equal to the `dimension` argument value.

### media-query-min(dimension: **string**)

Create a media query where the min-width will be equal to the `dimension` argument value.

### media-query-range(dimension1: **string**, dimension2: **string**)

Create a media query where the min-width will be equal to the `dimension1` value, and max-width will be the `dimension2` argument value.

### font-size(size: **string**)

Converts a pixel based size to REM and returns both sizes (px and rem) in order to be backward compatible.

## Classes

### Padding and Margin

The `padding` and `margin` classes implement the BEM methodology.

For the block, you can specify the `padding` or `margin` as a prefix.

The element represents the side of the element that the style will be applied:
* __top: Apply only to top
* __bottom: Apply ony to bottom
* __topbottom: Apply to top and bottom
* __left: Apply only to left
* __right: Apply only to right
* __leftright: Apply to left and right

The modifier represents the amount of pixels that will be set for that side. The pixels can be applied using a step of 5px, and can be used on a range from 5px to 60px.

The end class will be something like `margin__topbottom--45`. This example will apply a margin of 45px to the top and bottom of an element.

## Functions

### calculateRem(size: **string**)

Convert a given size in pixels to REM units, having in mind that the default font size on html is 100%, equivalent to 16px.

## Contributing

Want to contribute? We'd love that!

If you have a feature request or bug to report, please fill out a [GitHub Issue](https://github.com/luisfbmelo/sass-base-lm/issues) to begin the conversation.

## License

This project is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).