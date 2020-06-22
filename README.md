# Checkboxes

A library for customizable checkboxes ✅

[Demo](http://checkboxes.yifanai.com) 👈

## Background

Different browsers have different implementations for checkboxes:

See [this post](https://stackoverflow.com/questions/24322599/why-cannot-change-checkbox-color-whatever-i-do) about not able to style checkboxes. 😭

![](assets/safari.jpg) ![](assets/chrome.jpg) ![](assets/firefox.jpg) ![](assets/opera.jpg) ![](assets/edge.jpg)

Chrome uses the thick white tick, while Safari, Opera, Edge and Firefox all use the thin white tick. 😢

Safari, Opera and Edge use user's preferred Accent colour (from System Preferences on a Mac) as background for the checkboxes, whereas Chrome and Firefox stick with blue background. 🤯

![](assets/preferences.jpg)

These checkboxes by browsers are styled by User Agent style sheets and they can not be overridden easily. 😕 \
Thus, these checkboxes can hardly match the logo and theme colour of a website or a system! 😩

After some work, I successfully styled the checkboxes for our company's website. 😀 \
See [my reflection tweet](https://twitter.com/allenlearnit/status/1273599758129483776).

I would like to style them with ease in the future and for everyone, hence the creation of this small side project. 🙌

![](assets/checkboxes.gif)

There are now a couple of customizable options for the checkboxes. And many more to come!

## Getting Started

### Using CDN

Add this line to HTML file

```
<link rel="stylesheet" type="text/css" href="https://unpkg.com/checkboxes@1.1.3/dist/css/checkboxes.min.css">
```

✅

### Using NPM

Install checkboxes package using npm

```
npm i checkboxes
```

then add this line to HTML file

```
<link rel="stylesheet" type="text/css" href="checkboxes/dist/css/checkboxes.min.css">
```

✅

## Usage

Add "checkbox" class to the checkbox input. \
(Optionally, add custom styles to the element to change it from the default styles.)

i.e. \
from

```
<input type="checkbox">
```

to

```
<input type="checkbox" class="checkbox"
style="--size: {NUMBER}px; --radius: {NUMBER}px; --bg: #{RRGGBB}; --color: #{RRGGBB}; --time: {NUMBER}s;" {checked}>
```

e.g.

```
<input type="checkbox" class="checkbox"
style="--size: 20px; --radius: 8px; --bg: #000000; --color: #F47A37; --time: 0.4s;">
```

where the default style is
```
--size: 12px;
--radius: calc(var(--size) / 10);
--bg: red;
--color: white;
--time: 0.5s;
```

## Package Structure

```
.
|-- LICENSE
|-- README.md
|-- dist
|   `-- css
|       `-- checkboxes.min.css
|-- gulpfile.js
|-- package-lock.json
|-- package.json
`-- src
    |-- checkboxes.html
    `-- scss
        |-- checkboxes.css
        |-- checkboxes.css.map
        `-- checkboxes.scss
```

## Authors

* **Yifan Ai** - *Initial work*

See also the list of [contributors](https://github.com/ayfallen/checkboxes/graphs/contributors) who participated in this project.

## License

This project is licensed under the MIT License
