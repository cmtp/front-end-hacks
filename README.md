# front-end-hacks
## Tools
- chrome developer tools
- [visual studio code](https://code.visualstudio.com/)
- [Udacity Feedback Chrome Extension](https://github.com/udacity/frontend-grading-engine)

## Web Mobile First Concepts
- Viewport size - Defines the area of the screen that the browser render content too.
- Device Pixel Ratio - is the ratio between physical pixels and logical pixels.
- DIP: Devices independent pixels = Hardware Pixels * (1 css pixel/DPR)
- User Agent - This is a technical data about the device and software that the visitor is using.

## Responsive Tricks

- Always set viewport!

```html
<meta name="viewport" content="width=device-width,initial-scale=1.0">
```
- Always set the max-width for tags: img, embed, object, video
```css
img, embed, object, video {
    max-width: 100%;
}
```
- the minimun width of the devices is 320px, less than its is responsive
- Tap targets should be have 48px for height and 48px for width, for do more easily touch them, FI.:
```css
nav a, button {
    min-width: 48px;
    min-height: 48px;
}
```
- Apply first mobile, start development with the smallest screen and end with the largest screen, this is a good practice and help to improve in performance

## Media queries
- Media quieres are your friend!
- Add media queries:

1. First option. use media attribute into html (many small files and many http requests)

```html
<link rel="stylesheet" media="screen and (min-width:320px)" href="mobile.css">
<link rel="stylesheet" media="screen and (min-width:768px)" href="tablet.css">
<link rel="stylesheet" media="screen and (min-width:1024px)" href="desktop.css">
```

2. Use @media into css code (big files and few http requests)
```css

@media screen and (min-width:320px) {
    // mobile
}
@media screen and (min-width:768px) {
    // tablet
}
@media screen and (min-width:1024px) {
    // desktop
}
```

3. use @import (not recommendded for performance)

```css
@import url("mobile.css") only screen and (min-width:320px);
```

- Use <code>max-width</code> and <code>min-width</code> instead of <code>max-device-width</code> and <code>min-device-width</code> in media queries
- Pick breakpoints for media queries acordding to the content of application
- We can apply complex media queries like this:

```css
@media only screen and (min-width:500px) and (max-width:600px) {
    // css content
}
```

## Flexbox
- Flexbox is one of the most powerfull tools for the layout
```html
<!-- styles -->
<style>
.container {
    width:100%;
    display: flex;
}
.box {
    width: 150px;
}
</style>
<!-- html -->
<div class="container">
    <div class="box dark_blue"></div>
    <div class="box light_blue"></div>
    <div class="box green"></div>
</div>
```

-   Use <code>flex-wrap: wrap</code> in the <code>.container</code> style for wrap the content to the next line
- Use <code>order</code> style in the container's child for apply order for the elements FI: <code>order: 1</code>
- Use width on percentage
