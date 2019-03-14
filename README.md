# SCSS Starterkit

A modular and customizable base for SCSS compiled website, only created for my personal needs and habits.

## Table of contents

+ [Usage](https://github.com/quentin-f451/scss-base#usage)
+ [List of variables](https://github.com/quentin-f451/scss-base#list-of-variables)
+ [List of classes](https://github.com/quentin-f451/scss-base#list-of-classes)
  + [Simple, non-variable classes](https://github.com/quentin-f451/scss-base#simple-non-variable-classes)
  + [Variable classes](https://github.com/quentin-f451/scss-base#variable-classes)
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

### Default breakpoint values

The default values for responsive **breakpoints** *in px*.
+ `$screen-xxs` XXtra Small minimum screen width — Default: `375`
+ `$screen-xs` Xtra Small minimum screen width — Default: `480`
+ `$screen-sm` Small minimum screen width — Default: `768`
+ `$screen-md` Medium minimum screen width — Default: `1024`
+ `$screen-lg` Large minimum screen width — Default: `1300`
+ `$screen-xl` Xtra Large minimum screen width — Default: `1500`
+ `$screen-xxl` XXtra Large minimum screen width — Default: `1800`

## List of classes

+ Simple, non-variable classes: [Text](https://github.com/quentin-f451/scss-base/tree/master#text), [Display](https://github.com/quentin-f451/scss-base/tree/master#display), [Overflow](https://github.com/quentin-f451/scss-base/tree/master#overflow), [Position](https://github.com/quentin-f451/scss-base/tree/master#position)
+ Variable classes: [Column layout](https://github.com/quentin-f451/scss-base#column-layout), [Margins, paddings, positioning](https://github.com/quentin-f451/scss-base#margins-paddings-positioning), [Colors](https://github.com/quentin-f451/scss-base#colors), [Z-Index](https://github.com/quentin-f451/scss-base#z-index), [Height and width](https://github.com/quentin-f451/scss-base#height-and-width), [Transition](https://github.com/quentin-f451/scss-base#transition), [Fonts](https://github.com/quentin-f451/scss-base#fonts), [Typesetting](https://github.com/quentin-f451/scss-base#typesetting)

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

### Variable classes

#### Column layout

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

#### Margins, paddings, positioning

Depending on the value of the variables `$is-global-viewport-sizes`, `$base-margin`, `$base-padding` and `$base-absolute`. With `{number}` between `0` and `10`.

```css
.margin-{number} {
  margin: 1px * {$base-margin} * {number};
}
.margin-t-{number} {
  margin-top: 1px * {$base-margin} * {number};
}
.margin-r-{number} {
  margin-right: 1px * {$base-margin} * {number};
}
.margin-b-{number} {
  margin-bottom: 1px * {$base-margin} * {number};
}
.margin-l-{number} {
  margin-left: 1px * {$base-margin} * {number};
}
.margin-x-{number} {
  margin-right: 1px * {$base-margin} * {number};
  margin-left: 1px * {$base-margin} * {number};
}
.margin-y-{number} {
  margin-top: 1px * {$base-margin} * {number};
  margin-bottom: 1px * {$base-margin} * {number};
}
.padding-{number} {
  padding: 1px * {$base-padding} * {number};
}
.padding-t-{number} {
  padding-top: 1px * {$base-padding} * {number};
}
.padding-r-{number} {
  padding-right: 1px * {$base-padding} * {number};
}
.padding-b-{number} {
  padding-bottom: 1px * {$base-padding} * {number};
}
.padding-l-{number} {
  padding-left: 1px * {$base-padding} * {number};
}
.padding-x-{number} {
  padding-right: 1px * {$base-padding} * {number};
  padding-left: 1px * {$base-padding} * {number};
}
.padding-y-{number} {
  padding-top: 1px * {$base-padding} * {number};
  padding-bottom: 1px * {$base-padding} * {number};
}
.top-{number} {
  top: 1px * {$base-padding} * {number};
}
.right-{number} {
  right: 1px * {$base-padding} * {number};
}
.bottom-{number} {
  bottom: 1px * {$base-padding} * {number};
}
.left-{number} {
  left: 1px * {$base-padding} * {number};
}
```

For example, for `$base-margin: 10`:

```css
.margin-4 {
  margin: 40px;
}
.margin-x-8 {
  margin-top: 80px;
  margin-bottom: 80px;
}
```

If `$is-global-viewport-sizes` is set to `true`, the formula to get the margin will change from `1px * {$base-padding} * {number}` to `1rem * {$line-height-default} * {$base-padding} * {number}`. For example, for `$base-padding: 1` and `$line-height-default: 1.25`:

```css
.padding-3 {
  padding: 3.75rem;
}
.padding-r-6 {
  padding-right: 7.5rem;
}
```

#### Colors

Depending on the value of the variables `$text-color`, `$primary-color`, `$secondary-color`, `$tertiary-color` and `$background-color`.

```css
.text-color {
  color: {$text-color};
}
.background-color {
  background-color: {$background-color};
}
.color-1 {
  color: {$primary-color};
}
.color-2 {
  color: {$secondary-color};
}
.color-3 {
  color: {$tertiary-color};
}
.bg-color-1 {
  background-color: {$primary-color};
}
.bg-color-2 {
  background-color: {$secondary-color};
}
.bg-color-3 {
  background-color: {$tertiary-color};
}
```

#### Z-Index

With `{number}` between `0` and `10`.

```css
.z-{number} {
  z-index: {number};
}
.z-neg-{number} {
  z-index: -{number};
}
```

For example:

```css
.z-8 {
  z-index: 8;
}
.z-neg-5 {
  z-index: -5;
}
```

#### Height and width

With `{number}` between `0` and `10`.

```css
.width-{number} {
  width: {number} * 10%;
}
.height-{number} {
  height: {number} * 10%;
}
```

For example:

```css
.width-4 {
  width: 40%;
}
.height-8 {
  height: 80%;
}
```

#### Transition

Depending on the value of the variables `$base-transition-selector`, `$base-transition-speed` and `$base-transition-type`.

```css
.base-transition {
  transition: {$base-transition-selector} {$base-transition-speed} {$base-transition-type};
  -moz-transition: {$base-transition-selector} {$base-transition-speed} {$base-transition-type};
  -webkit-transition: {$base-transition-selector} {$base-transition-speed} {$base-transition-type};
  -o-transition: {$base-transition-selector} {$base-transition-speed} {$base-transition-type};
}
```

#### Fonts

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
```

#### Typesetting

Depending on the value of the `$text-` and `$line-` kinds of variables.

```css
.text-xxs{
  font-size: {$text-xxs};
}
.text-xs{
  font-size: {$text-xs};
}
.text-sm{
  font-size: {$text-sm};
}
.text-md{
  font-size: {$text-md};
}
.text-lg{
  font-size: {$text-lg};
}
.text-xl{
  font-size: {$text-xl};
}
.text-xxl{
  font-size: {$text-xxl};
}
.line-xxs{
  line-height: {$line-xxs};
}
.line-xs{
  line-height: {$line-xs};
}
.line-sm{
  line-height: {$line-sm};
}
.line-md{
  line-height: {$line-md};
}
.line-lg{
  line-height: {$line-lg};
}
.line-xl{
  line-height: {$line-xl};
}
.line-xxl{
  line-height: {$line-xxl};
}
```

## To-do

+ [x] Optimize the classes
+ [ ] Make it easier to install
+ [ ] Test it on a real project
