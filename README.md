# SCSS Base

A modular and customizable base for SCSS compiled website, only created for my personal needs and habits.

## Table of contents

+ [Usage](https://github.com/quentin-f451/scss-base#usage)
+ [List of variables](https://github.com/quentin-f451/scss-base#list-of-variables)
+ [List of classes](https://github.com/quentin-f451/scss-base#list-of-classes)
+ [To-do](https://github.com/quentin-f451/scss-base#to-do)

## Usage

Add this to any project with compiled SCSS.

1. Fill in the `config.scss` file with your values.
2. Add your own modules and `.scss` files in `_modules` folder.
3. Link them at the end of the `application.scss` file
```css
@import "_modules/name_of_the_module.scss";
```
4. Compile

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
+ `$primary-fallback` Primary fallback font (applied by default to `html, body`) — No default value, it can be any name.
+ `$secondary-font-family` Secondary font — No default value, it can be any name.
+ `$secondary-fallback` Secondary fallback font — No default value, it can be any name.
+ `$tertiary-font-family` Tertiary font — No default value, it can be any name.
+ `$tertiary-fallback` Tertiary fallback font — No default value, it can be any name.

### Default layout values

+ `$number-of-columns` Number of **columns** that divide the width of the container. It can be applied at any level in the code. — Default: `12`
+ `$is-global-viewport-sizes` `true` or `false`. `true` will define `$base-margin`, `$base-padding` and `$base-absolute` in `unitless` values relatively to `$line-height-default`, `false` will define `$base-margin`, `$base-padding` and `$base-absolute` in `px` values. - Default: `false`

If `$is-global-viewport-sizes` is set to `true`, the three following variables are `unitless`. If `$is-global-viewport-sizes` is set to `false`, the three following variables are in `px`.
+ `$base-margin` Default **margin** value *in px* or *unitless*. - Default: `10`
+ `$base-padding` Default **padding** value *in px* or *unitless*. - Default: `10`
+ `$base-absolute` Default **absolute positioning** value (`top`, `bottom`, `right` and `left`) *in px* or *unitless*. - Default: `10`

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

## List of classes

+ Simple, non-variable classes: [Text](https://github.com/quentin-f451/scss-base/tree/master#text), [Display](https://github.com/quentin-f451/scss-base/tree/master#display), [Overflow](https://github.com/quentin-f451/scss-base/tree/master#overflow), [Position](https://github.com/quentin-f451/scss-base/tree/master#position)
+ Variable classes:

### Simple, non-variable classes

#### Text

 ```css
.text-l {
  text-align: left;
}
.text-r {
  text-align: right;
}
.text-c {
  text-align: center;
}
.justify {
  text-align: justify;
  -ms-word-break: normal;
  word-break: normal;
  word-break: break-word;
  -webkit-hyphens: auto;
  -moz-hyphens: auto;
  hyphens: auto;
}
.uppercase {
  text-transform: uppercase;
}
.lowercase {
  text-transform: lowercase;
}
.hyphen {
  -ms-word-break: normal;
  word-break: normal;
  word-break: break-word;
  -webkit-hyphens: auto;
  -moz-hyphens: auto;
  hyphens: auto;
}
.no-hyphen {
  -webkit-hyphens: none;
  -moz-hyphens: none;
  hyphens: none;
  -ms-hyphens: none;
}
 ```

#### Display

 ```css
.disp-b {
  display: block;
}
.disp-ib {
  display: inline-block;
}
.disp-f {
  display: flex;
}
.disp-if {
  display: inline-flex;
}
.disp-n {
  display: none;
}
 ```

#### Overflow

 ```css
.scroll {
  overflow: scroll;
}
.scroll-x {
  overflow-x: scroll;
}
.scroll-y {
  overflow-y: scroll;
}
.no-scroll {
  overflow: hidden;
}
.no-scroll-x {
  overflow-x: hidden;
}
.no-scroll-y {
  overflow-y: hidden;
}
 ```

#### Position

 ```css
.pos-a {
  position: absolute;
}
.pos-r {
  position: relative;
}
.pos-f {
  position: fixed;
}
.pos-s {
  position: sticky;
}
 ```

## To-do

+ [ ] Optimize the classes
+ [ ] Test it on a real project
