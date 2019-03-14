# SCSS Starterkit
[![Release](https://img.shields.io/github/release-pre/quentin-f451/scss-starterkit.svg)](https://github.com/quentin-f451/scss-starterkit/releases)

A modular and customizable base for SCSS compiled website, only created for my personal needs and habits.

## Table of contents

+ [Usage](#usage)
  + [If you don't use my starterkits](#if-you-dont-use-my-starterkits)
  + [If you use my starterkits](#if-you-use-my-starterkits)
+ [List of variables](#list-of-variables)
+ [List of classes](#list-of-classes)

## Usage

### If you don't use my starterkits 

1. Create your `scss` folder.
2. Add this repo as a submodule 
```
git add submodule https://github.com/quentin-f451/scss-starterkit _base
```
3. Create your `config.scss` file with the following content:
```scss
// CONFIGURATE DOCUMENT

// FONT SIZES

$text-default-px:                           16;       // Default font-size in px (default: 16px)
$line-height-default:                       1.25;     // Default line-height, relative to default font-size (default: 1.25)

// Viewport values
$is-global-viewport-text:                   true;     // true for font-size globally defined in vw, false for font-size globally defined in px
$viewport-width-px:                         1280;     // Screen size used for calculating font-size in vw (like http://emilolsson.com/tools/vw-unit-calc-an-online-responsive-css-font-size-calculator/)

// Font sizes - can be any unit
$text-xxs:                                  0.5rem;   // (default: 0.5rem)  -- small
$text-xs:                                   0.75rem;  // (default: 0.75rem) -- h6
$text-sm:                                   1.0rem;   // (default: 1.0rem)  -- h5
$text-md:                                   1.5rem;   // (default: 1.5rem)  -- h4
$text-lg:                                   2.0rem;   // (default: 2.0rem)  -- h3
$text-xl:                                   3.0rem;   // (default: 3.0rem)  -- h2
$text-xxl:                                  6.0rem;   // (default: 6.0rem)  -- h1

// Line height - realtive to font-size
$line-xxs:                                  1.0;      // (default: 1.0)
$line-xs:                                   1.125;    // (default: 1.125)
$line-sm:                                   1.25;     // (default: 1.25)
$line-md:                                   1.375;    // (default: 1.375)
$line-lg:                                   1.5;      // (default: 1.5)
$line-xl:                                   2.0;      // (default: 2.0)
$line-xxl:                                  3.0;      // (default: 3.0)

// __________________________________________________________ //

// FONTS

$primary-font-family:                       '';
$primary-font-url:                          '';       // Without extension
$primary-fallback:                          'Times New Roman', Times, serif;
$secondary-font-family:                     '';
$secondary-font-url:                        '';       // Without extension
$secondary-fallback:                        Garamond, 'Hoefler Text', 'Times New Roman', Times, serif;
$tertiary-font-family:                      '';
$tertiary-font-url:                         '';       // Without extension
$tertiary-fallback:                         'Helvetica Neue', Helvetica, Arial, 'Lucida Grande', sans-serif;

/*
Fallbacks examples
 - 'Times New Roman', Times, serif
 - Garamond, 'Hoefler Text', 'Times New Roman', Times, serif
 - 'Helvetica Neue', Helvetica, Arial, 'Lucida Grande', sans-serif
 - 'Courier New', Courier, monospace
*/

// __________________________________________________________ //

// LAYOUT

$number-of-columns:                         12;       // Number of columns

// Base space
$base-space:                                10px;     // Initial space in px (default: 10px)

// __________________________________________________________ //

// COLORS

$text-color:                                black;    // Text color
$link-color:                                blue;     // Link color
$hover-color:                               red;      // Hover color

$primary-color:                             black;    // Color 1
$secondary-color:                           black;    // Color 2
$tertiary-color:                            black;    // Color 3
$background-color:                          white;    // Background color

// __________________________________________________________ //

// TRANSITION

$base-transition-selector:                  all;
$base-transition-speed:                     .3s;
$base-transition-type:                      ease-in-out;

// __________________________________________________________ //

// BREAKPOINTS

$screen-xs:                                 0px;        // (default: 0px)
$screen-sm:                                 576px;      // (default: 576px)
$screen-md:                                 1000px;     // (default: 1000px)
$screen-lg:                                 1200px;     // (default: 1200px)
$screen-xl:                                 1500px;     // (default: 1500px)
$screen-xxl:                                1800px;     // (default: 1800px)

// __________________________________________________________ //

// FREE CONFIG
```

4. Create your `application.scss` file with the following content:
```scss
// GLOBAL SCSS

// IMPORT LIBRARIES
@import "_base/_lib/_normalize.scss";     // Normalize.css - CSS Reset

//IMPORT CONFIG
@import "config";                   // Initial values

// IMPORT PARTIALS
@import "_base/_partials/_mediaqueries";  // Initiate mediaqueries
@import "_base/_partials/_base";          // Initiate basic elements
@import "_base/_partials/_fonts";         // Initiate fonts
@import "_base/_partials/_grid";          // Initiate grid
@import "_base/_partials/_margins";       // Initiate margins and padding
@import "_base/_partials/_type";          // Initiate type

// IMPORT MODULES
// Add here the scss files for the website
```

### If you use my starterkits 

1. Simply change the values of the `config.scss` file.

## List of variables

All these variables can be changed in the `config.scss` file.

### Default text values

+ `$text-default-px` Default **font-size** *in px* (applied by default to `html, body`) — Default: `16`
+ `$line-height-default` Default *unitless* **line-height** (applied by default to `html, body`) — Default: `1.25`
+ `$is-global-viewport-text` `true` or `false`. `true` will convert `html, body` font-size to `vw` responsive unit, `false` will let `html, body` font-size in `px`. - Default: `true`
+ `$viewport-width-px` Referencial wiewport width to convert `html, body` font-size in `vw` responsive unit. Will only have effect of `$is-global-viewport-text` is set to `true`. See [here](http://emilolsson.com/tools/vw-unit-calc-an-online-responsive-css-font-size-calculator/) for explanation on viewport font-size unit. - Default: `1280`

### Default font sizes

The default font sizes can be set in *any unit*. By default, font sizes are set in `rem`, so relatively to `$text-default-px`. **These are the only variable that need a unit specified directly in the variable**.
+ `$text-xxs` XXtra Small font-size (applied by default to `small`) — Default: `0.5rem`
+ `$text-xs` Xtra Small font-size (applied by default to `h6`) — Default: `0.75rem`
+ `$text-sm` Small font-size (applied by default to `h5`) — Default: `1.0rem` = `$text-default-px`
+ `$text-md` Medium font-size (applied by default to `h4`) — Default: `1.5rem`
+ `$text-lg` Large font-size (applied by default to `h3`) — Default: `2.0rem`
+ `$text-xl` Xtra Large font-size (applied by default to `h2`) — Default: `3.0rem`
+ `$text-xxl` XXtra Large font-size (applied by default to `h1`) — Default: `6.0rem`

### Default line heights

The default line height are set *unitless*, relative to text. See [here](https://css-tricks.com/almanac/properties/l/line-height/).
+ `$line-xxs` XXtra Small line-height — Default: `1.0`
+ `$line-xs` Xtra Small line-height — Default: `1.125`
+ `$line-sm` Small line-height (applied by default to `html, body`) — Default: `1.25`
+ `$line-md` Medium line-height — Default: `1.375`
+ `$line-lg` Large line-height — Default: `1.5`
+ `$line-xl` Xtra Large line-height — Default: `2.0`
+ `$line-xxl` XXtra Large line-height — Default: `3.0`

### Default font values

Fonts need to be linked in the `_partials/_fonts.scss` file. Their name will be the one you choose in the variables.
+ `$primary-font-family` Primary font (applied by default to `html, body`) — No default value, it can be any name.
+ `$primary-font-url` Primary font URL.
+ `$primary-fallback` Primary fallback font (applied by default to `html, body`) — No default value, it can be any name.
+ `$secondary-font-family` Secondary font — No default value, it can be any name.
+ `$secondary-font-url` Secondary font URL.
+ `$secondary-fallback` Secondary fallback font — No default value, it can be any name.
+ `$tertiary-font-family` Tertiary font — No default value, it can be any name.
+ `$tertiary-font-url` Tertiary font URL.
+ `$tertiary-fallback` Tertiary fallback font — No default value, it can be any name.

### Default layout values

+ `$number-of-columns` Number of **columns** that divide the width of the container. It can be applied at any level in the code. — Default: `12`
+ `$base-space` Default **space** value *in px*. - Default: `10px`

### Default color values

Colors can be set in any kind of css way. (Ex: `black` or `#000000` or `#000` or `rgba(0,0,0,1)`).
+ `$text-color` Default **text** color (applied by default to `html, body`) — Default: `black`
+ `$link-color` Default **link** color (applied by default to `a`) — Default: `blue`
+ `$hover-color` Default **link hover** color (applied by default to `a:hover`) — Default: `red`
+ `$primary-color` Primary color — Default: `black`
+ `$secondary-color` Secondary color — Default: `black`
+ `$tertiary-color` Tertiary color — Default: `black`
+ `$background-color` Default **background** color (applied by default to `html, body`) — Default: `white`

### Default transition values

The default values for globally set **transitions**.
+ `$base-transition-selector` Default **selector** for transitions — Default: `all`
+ `$base-transition-speed` Default **speed** for transitions — Default: `.3s`
+ `$base-transition-type` Default **type** of transition — Default: `ease-in-out`

### Default breakpoint values

The default values for responsive **breakpoints** *in px*.
+ `$screen-xs` Xtra Small minimum screen width — Default: `0px`
+ `$screen-sm` Small minimum screen width — Default: `576px`
+ `$screen-md` Medium minimum screen width — Default: `1000px`
+ `$screen-lg` Large minimum screen width — Default: `1200px`
+ `$screen-xl` Xtra Large minimum screen width — Default: `1500px`
+ `$screen-xxl` XXtra Large minimum screen width — Default: `1800px`

## List of classes

[Column layout](https://github.com/quentin-f451/scss-base#column-layout), [Margins, paddings, positioning](https://github.com/quentin-f451/scss-base#margins-paddings-positioning), [Fonts](https://github.com/quentin-f451/scss-base#fonts)

### Column layout

Depending on the number of columns set at `$number-of-columns`, three types of classes allow to work on column layouts.
`.col-` to specify the width of a `div` with a number of columns. `.sub-` to specify a subdivision by a certain number. `.off-` to specify a `margin-left` value with a number of columns.

```css
.col-{number} {
  width: 100 / {$number-of-columns} * {number}%;
}
.sub-{number} {
  width: 100 / {number}%;
}
.off-{number} {
  margin-left: 100 / {$number-of-columns} * {number}%;
}
```

`{number}` must be between `1` and `$number-of-columns`. For example, for `$number-of-columns: 12`:

```css
.col-3 {
  width: 25%;
}
.sub-3 {
  width: 33.33333%;
}
.off-3 {
  margin-left: 25%;
}
```

### Margins, paddings, positioning

Depending on the value of the variables `$base-space`.

```css
@include margin({number});
@include absolute({number});
@include padding({number});
```

For example, for `$base-space: 10`, it will be compiled as:

```css
@include margin(2);
margin-top: 20px;
margin-right: 20px;
margin-bottom: 20px;
margin-left: 20px;

@include absolute(2 1);
top: 20px;
right: 10px;
bottom: 20px;
left: 10px;

@include padding(2 1 5 7);
padding-top: 20px;
padding-right: 10px;
padding-bottom: 50px;
padding-left: 70px;
```

### Fonts

Depending on the value of the variables `$primary-font-family`, `$secondary-font-family`, `$tertiary-font-family`, `$primary-fallback`, `$secondary-fallback` and `$tertiary-fallback`.

```css
.font-1 {
  font-family: {$primary-font-family}, {$primary-fallback};
}
.font-2 {
  font-family: {$secondary-font-family}, {$secondary-fallback};
}
.font-3 {
  font-family: {$tertiary-font-family}, {$tertiary-fallback};
}
``
