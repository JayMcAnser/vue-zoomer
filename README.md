# vue-zoomer

> Zoom the image or other thing with mouse or touch
For the original documentatie see: https://github.com/jarvisniu/vue-zoomer/

This adjusted version adds extra events to handle the redraw of the scrolled aera so all markers placed on the background
will not be resize.

## .API

### v-zoomer&gt; Properties

* scale - Number the current scale mode

### v-zoomer&gt; Events

* updated:zoomed - called when zoomed (true: scalled, false: not scaled)
* update:start - called before any changes is applied
* update:end - called when the zoom is finishe
* swipe - (direction) direction = [left|right]

## contributor

updated by JayMcAnser

## License

MIT
