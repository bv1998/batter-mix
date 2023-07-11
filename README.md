# Batter Mix

![version](https://badgen.net/static/V/1.2.0/)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

This is a mixins scss file and library that will be imported into your project and be able to be included as a way to save time and lines of code. This was created as a personal and workflow project.

_Having any problems and want to contribute? Feel free to slack me or email me_.

### _How to Use_

To use in your project you will need to use the scss function of import. In order to use the code below it must be in the same folder as your main .scss file.

```scss
@import "mixins";
```

or

```scss
@import "mixins.scss";
```

## Includes:

### `backgroundOverlay`

This is used to make an overlay over the bakcground of a div. This will create an ::after and then put the set bakcground and overlay to what is passed through the mixin

```scss
@include backgroundOverlay($backgroundSetting, $overlayOpacity: 100%);
```

`$backgroundSetting`: use this to set anything you would after 'background:' in scss. So this can be a color, gradient or even url.

`$overlayOpacity`: use this to set the opacity for this overlay. By default this is set to 100% so if you want it to be 100% then you do not need to pass this variable.

### `flickityButtonIcon`

This is used to style the button of a flickity slider using the button already there and adding an after on the button itself as the icon. To use this you need to have your icon that is used, facing right.

```scss
@include flickityButtonIcon($backgroundColor, $icon, $iconColor, $iconPosition, $buttonSize, $hoverbgColor, $hoverIconColor, $borderColor, $hoverborder);
```

`$backgroundColor`: This is the color of the background of the button itself.

`$icon`: This will need to be a svg or png that will be used as a mask. The icon will need to be facing right and will automatically turn left through the code for the previous button.

`$iconColor`: Color of the icon.

`iconPosition`: The amount of px or percentage that the button is away from its origin point.

`$buttonSize`: This changes the size of the circle. The variable is used for both the height and width of the button background.

`$hoverbgColor`: This by default is set to the `$iconColor` however this can be set so the color of the background changes on hover.

`$hoverIconColor`: This is by default set to the `$backgroundColor` however this can be set so the color of the icon changes on hover.

`$borderColor`: This is by default set to the `$backgroundColor` however this can be set so the color of the border is different on the button than the background color.

`$hoverborder`: This is by default set to the `$iconColor` however this can be set so the color of the border is different on the button than the background color on hover.

### `centerFlex`

This is just one line to center the items in div using flex

```scss
@include centerFlex();
```

### `socialCircle`

This is to add a circle background and have the social icons in the middle

```scss
@include socialCircle( $circleSize, $backgroundColor, $hoverBackground, $iconColor, $hoverIconColor);
```

`$circleSize`: This is the size of the background of the social icon

`$backgroundColor`: This is the color of the background of the button itself.

`$hoverBackground`: This is the color of the background changes on hover.

`$iconColor`: Color of the icon.

`$hoverIconColor`: This is by default set to the $icon color so if you want just the bakcgroudn to change you do not need to put this variable in the mixin.

### `svgMask`

This is to add an svg mask to a div. If you are okay with all of the defaults the only variable that needs to be passed through is simply the url for the variable `$svg`

```scss
@include svgMask($svg, $maskSize, $maskPosition, $maskRepeat);
```

`$svg`: Put the url to either an svg orpng with transparent bakcground here and this will be the mask.

`$maskSize`: This is by default set to 'contain' but changes the size of the mask in the div just like background-position.

`$maskPosition`: By default is set to 'center center'

`$maskRepeat`: By default set to 'no-repeat'

### `fontSettings`

This is just to default font settings with the information in the xd

```scss
@include fontSettings($fontSize, $fontWeight, $lineHeightPx, $textColor);
```

`$fontSize`: Just put the pixel value number, no need to put the px after and then it will run through rem function written by [Michael Palcowski](https://github.com/MichaelPalcowski) so that way it can be in the rem format.

`$fontWeight`: Fiont weight number

`$lineHeightPx`: When working with Adobe XD, the line height is displayed in the pizxel format, i norder to combat that you put that number in here and using the calc function then it will make the correct line height.

`$textColor`: The color of the text, but does not include the !important if that is necessary then you will have to write that below.
