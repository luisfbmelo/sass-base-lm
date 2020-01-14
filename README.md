# SASS Base by Luis Melo

This code base is intended to be used as a basis for your project, using SASS.

Includes:
* Mixins
  * Media Queries
  * Animations with keyframes
  * Transitions
  * Opacity
  * Border Radius
  * Transforms
  * Scale
  * Translates
  * Calculated REM font-size
* Margins and paddings with 5px steps
* Colors functions to display with variants

# Install

```npm install sass-base-lm --save-dev``` 

or 

```yarn add sass-base-lm --dev```

# Use

In your root SASS file, just require the `styles.scss`:
```
//  Without Webpack
@import 'node_modules/sass-base-lm/assets/styles';

//  With Webpack
@import '~/node_modules/sass-base-lm/assets/styles';
```

## License

This project is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).