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
