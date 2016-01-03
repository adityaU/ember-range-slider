# Ember Range Slider [![Build Status](https://travis-ci.org/collectrium/ember-range-slider.svg?branch=master)](https://travis-ci.org/collectrium/ember-range-slider) [![Ember Observer Score](http://emberobserver.com/badges/ember-range-slider.svg)](http://emberobserver.com/addons/ember-range-slider)

This ember-cli addon provides a horizontal slider component with two handles that allows for visually selecting a range from within a specified min and max.

[TODO: Animated GIF here]

Supported interactions include pressing (or touching) and dragging either handle, as well as tapping on the slider track to adjust the nearest slider handle to the new location.

The component follows a data down / actions up approach and uses hammer.js to handle the touch and mouse interactions.

## Live Demo

View a live demo here: [http://collectrium.github.io/ember-range-slider/](http://collectrium.github.io/ember-range-slider/)

## Example

```hbs
{{ember-range-slider
  min=rangeMin
  max=rangeMax
  start=start
  end=end
  rangeChanging=(action 'rangeSliderChanging')
  rangeChanged=(action 'rangeChanged')
  isSlidingChanged=(action (mut isSliding))
}}
```

## Data down

`min` and `max` are numeric values that define the values associated with the left and right edge of the slider.

`start` and `end` are numeric values assigned to the left and right handle.

## Actions Up

The `rangeChanging` action is fired with start and end values continuously as the user slides a handle along the range.

The `rangeChanged` action is fired with start and end values when a range change is "committed", i.e. when the user releases the slider handle.

The `isSlidingChanged` action is fired with `true` as the user begins sliding a handle and again with `false` when the user releases the handle.

## Development Setup

### Installation

* `git clone` this repository
* `npm install`
* `bower install`

### Running Tests

* `ember try:testall`
* `ember test`
* `ember test --server`

*NOTE:* Tests currently run successfully in-browser, but not headless in PhantomJS due to an error with `new MouseEvent`. It would be fantastic to fix this.

### Running the dummy app

* `ember server`
* Visit your app at http://localhost:4200.

For more information on using ember-cli, visit [http://www.ember-cli.com/](http://www.ember-cli.com/).

## Credits

This addon was extracted from a prototype project at Collectrium. Contributions from @lukemelia, @chrislopresto and @leahdungo.
