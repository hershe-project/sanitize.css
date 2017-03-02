# sanitize.css <a href="https://github.com/jonathantneal/sanitize.css"><img src="https://jonathantneal.github.io/sanitize.css/logo.svg" alt="sanitize.css logo" width="80" height="80" align="right"></a>

[![NPM Version][npm-img]][npm-url]
[![Bower Version][bow-img]][bow-url]
[![CDNJS Version][cdn-img]][cdn-url]
[![Build Status][cli-img]][cli-url]
[![License][lic-img]][lic-url]
[![Gitter Chat][git-img]][git-url]

[sanitize.css] is a CSS library that corrects broken and missing styles in all
browsers, preserving useful defaults rather than unstyling everything. It’s
developed alongside [normalize.css], so every normalization includes the
browsers or browser versions being targeted, and every opinionated change is
marked and documented.

##### NPM

```sh
npm install --save sanitize.css
```

##### Bower

```sh
bower install --save sanitize-css
```

## Features

##### Backgrounds should not repeat by default

```css
* {
	background-repeat: no-repeat;
}
```

##### Box sizing should be inherited and default to border-box

```css
* {
	box-sizing: inherit;
}

html {
	box-sizing: border-box;
}
```

##### Cursor should only change to hint non-obvious interfaces

```css
html {
	cursor: default;
}
```

##### Regular text should be sans serif with a comfortable line height

```css
html {
	font-family: sans-serif
	line-height: 1.5;
}
```

##### Documents should not use a margin for outer padding

```css
body {
	margin: 0;
}
```

##### Navigation lists should not include a marker style

```css
nav ol, nav ul {
	list-style: none;
}
```

##### Text selections should not include text shadows

```css
::selection {
	text-shadow: none;
}
```

##### Media elements should align to the text center of other content

```css
audio, canvas, iframe, img, svg, video {
	vertical-align: middle;
}
```

##### SVGs should fallback to their surrounding text color

```css
svg {
	fill: currentColor;
}
```

##### Tables should not include additional border spacing

```css
table {
	border-collapse: collapse;
}
```

##### Form controls should be easily style-able

```css
button, input, select, textarea {
	background-color: transparent;
	color: inherit;
	font-size: inherit;
	line-height: inherit;
}
```

##### Textarea should only resize vertically by default

```css
textarea {
	resize: vertical;
}
```

##### Single taps should be dispatched immediately on clickable elements

```css
a, area, button, input, label, select, summary, textarea, [tabindex] {
	-ms-touch-action: manipulation;
	touch-action: manipulation;
}
```

##### ARIA roles should include visual cursor hints

```css
[aria-busy="true"] {
	cursor: progress;
}

[aria-controls] {
	cursor: pointer;
}

[aria-disabled] {
	cursor: default;
}
```

##### Visually hidden content should remain accessible

```css
[aria-hidden="false"][hidden]:not(:focus) {
	clip: rect(0, 0, 0, 0);
	display: inherit;
	position: absolute;
}
```

## Differences

[sanitize.css] styles elements more consistently with developers’ expectations
and preferences. [normalize.css] styles elements more consistently between
browsers. [reset.css] unstyles every element. Both sanitize.css and
normalize.css are maintained in sync, and both projects correct browser bugs
while carefully testing and documenting every change.

## Support

At present, sanitize.css supports the current and previous major releases of
popular web browsers. When a new version is released, we begin supporting that
newer version and stop supporting the third version back. Additionally, many
older browsers remain supported without supplementary CSS.

Currently tested and supported browsers in the latest release include
**Android 4.3-4.4+**, **Chrome 50-51+**, **Edge 12-13+**, **Firefox 46-47+**,
**Internet Explorer 10-11**, **iOS 7-8+**, **Opera 37-38+**, **Safari 8-9+**,
and **Windows Phone 8.1+**.

Additionally tested and supported browsers (requiring little supplementary CSS)
include **Internet Explorer 9** and **Safari 7**.

## License

**sanitize.css** is dedicated to the [public domain](LICENSE.md).

[bow-img]: https://img.shields.io/bower/v/sanitize-css.svg
[bow-url]: https://libraries.io/bower/sanitize-css
[cdn-img]: https://img.shields.io/cdnjs/v/10up-sanitize.css.svg
[cdn-url]: https://cdnjs.com/libraries/10up-sanitize.css
[cli-img]: https://img.shields.io/travis/jonathantneal/sanitize.css.svg
[cli-url]: https://travis-ci.org/jonathantneal/sanitize.css
[git-img]: https://img.shields.io/badge/chat-gitter-blue.svg
[git-url]: https://gitter.im/jonathantneal/sanitize.css
[lic-img]: https://img.shields.io/npm/l/sanitize.css.svg
[lic-url]: LICENSE.md
[npm-img]: https://img.shields.io/npm/v/sanitize.css.svg
[npm-url]: https://www.npmjs.com/package/sanitize.css

[normalize.css]: https://github.com/necolas/normalize.css
[reset.css]: http://meyerweb.com/eric/tools/css/reset/
[sanitize.css]: https://github.com/jonathantneal/sanitize.css
