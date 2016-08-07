# CSS Animations
Generic css animations written in LESS with compiling options. I created this with the intention of learning and understanding LESS better.

All the general animations I downloaded from [https://daneden.github.io/animate.css](https://daneden.github.io/animate.css/ "Animate.css").  
Additionally, the hover animations were downloaded from [http://ianlunn.github.io/Hover/](http://ianlunn.github.io/Hover/ "Hover.css").

----

## Table of Contents
1. [Installation](#installation)
  - [Linux Install](#linux-installation)
2. [Compiling](#compiling)
  - [Options](#options)
3. [Animations](#general-animations)
  - [General](#general-animations)
  - [Hover](#hover-2d-animations)
    - [2D](#hover-2d-animations)
    - [Background](#hover-background-animations)
    - [Border](#hover-border-animations)
    - [Misc](#hover-misc-animations)
4. [Thank You](#thank-you)

----

## Installation

To use lessc, you first need to [install npm](http://blog.npmjs.org/post/85484771375/how-to-install-npm).  
Once npm is installed, install lessc in your terminal by typing `npm install less -g`. To install a specific version, type `@VERSION` after the package name, ex. `npm install less@2.7.1 -g`.  
_Instructions from [lesscss.org](http://lesscss.org/usage/)_  
You can also install the clean css plugin to compile into a minified file. To do this, use `npm install -g less-plugin-clean-css`.

#### Linux Installation
On linux systems, when running the previous commands, you may need to use `sudo` to install the packages. Also, if you receive an error like `/usr/bin/env: node: no such file or directory` try using `ln -s /usr/bin/nodejs /usr/bin/node`, again you may need to use `sudo`. As described by [digitalmediums](https://github.com/digitalmediums) on [this post](https://github.com/nodejs/node-v0.x-archive/issues/3911), this error is often a misnaming error.

## Compiling
Compiled css file using lessc V2.7.1

To re-compile the css file, navigate to the root directory in your terminal and use `lessc animations.less css/animations.css` to overwrite the existing file.  
To re-compile the css file into a minified version, navigate to the root directory in your terminal and use `lessc --clean-css animations.less css/animations-min.css` to overwrite the existing file.

### Options
1. Durations: Set the duration variables. Animation is set to a slowDuration of 1s by default.  
2. Browser Prefixes: Set the prefixes that should be compiled.  
  - -webkit-  
  - -moz-  
  - -ms-  
  - -o-  
3. Animations to Compile: Set true next to each animation you want to use  
  - includeAllClasses defaults to true, set to false if you only want the keyframes to use in your own classes.  
4. Name Space: Prepends onto the hover classes. Default is 'hvr'.    
5. Colors: Default colors to be used for hover animations.

### General Animations

| Animation         | Main Class(es)                  | Variations/Add-Ons                                          |
| ----------------- | ------------------------------- | ----------------------------------------------------------- |
| Bounce            | `bounce`                        | none                                                        |
| Flash             | `flash`                         | none                                                        |
| Pulse             | `pulse`                         | none                                                        |
| Rubber Band       | `rubberBand`                    | none                                                        |
| Shake             | `shake`                         | none                                                        |
| Head Shake        | `headShake`                     | none                                                        |
| Swing             | `swing`                         | none                                                        |
| Ta Da!            | `tada`                          | none                                                        |
| Wobble            | `wobble`                        | none                                                        |
| Jello             | `jello`                         | none                                                        |
| Bounce In         | `bounceIn`, `bounceOut`         | `-down`, `-left`, `-right`, `-up`                           |
| Fade              | `fadeIn`, `fadeOut`             | `-down`, `-left`, `-right`, `-up`, `-big`                   |
| Flip              | `flip`                          | none                                                        |
| Flip In           | `flipInX`, `flipInY`            | none                                                        |
| Flip Out          | `flipOutX`, `flipOutY`          | none                                                        |
| Light Speed       | `lightSpeedIn`, `lightSpeedOut` | none                                                        |
| Rotate            | `rotateIn`, `rotateOut`         | `-downLeft`, `-downRight`, `-upLeft`, `-upRight`            |
| Hinge             | `hinge`                         | none                                                        |
| Roll              | `rollIn`, `rollOut`             | none                                                        |
| Zoom              | `zoomIn`, `zoomOut`             | `-down`, `-left`, `-right`, `-up`                           |
| Slide\*           | `slideIn`, `slideOut`           | `-down`, `-left`, `-right`, `-up`                           |
_\*Must use variation_

Add the `animated` class to your element to set the default animation speed or make sure you add an animation speed in the proper class.  
Add the `infinite` class to your element to play the animation indefinitely.  
Use the class variations by adding the dash and direction onto the main class. (Ex. `fadeIn-down`)  
To use the `-big` class variation, add it after the directional variation when available. (Ex. `fadeIn-down-big`)

### Hover 2D Animations

| 2D Animation       | Main Class(es)                  | Variations/Add-Ons                                                                                            |
| ------------------ | ------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| Grow               | `hvr-grow`                      | `-rotate`                                                                                                     |
| Shrink             | `hvr-shrink`                    | none                                                                                                          |
| Pulse              | `hvr-pulse`                     | `-grow`, `-shrink`                                                                                            |
| Push               | `hvr-push`                      | none                                                                                                          |
| Pop                | `hvr-pop`                       | none                                                                                                          |
| Bounce\*           | `hvr-bounce`                    | `-in`,`-out`                                                                                                  |
| Rotate             | `hvr-rotate`                    | none                                                                                                          |
| Float              | `hvr-float`                     | none                                                                                                          |
| Sink               | `hvr-sink`                      | none                                                                                                          |
| Bob                | `hvr-bob`                       | none                                                                                                          |
| Hang               | `hvr-hang`                      | `-down`, `-left`, `-right`, `-up`                                                                             |
| Skew               | `hvr-skew`                      | `-forward`, `-backward`                                                                                       |
| Wobble\*           | `hvr-wobble`                    | `-bottom`, `-top`, `-horizontal`, `-vertical`, `-skew`, `-bottomRight`, `-topRight`                           |
| Buzz               | `hvr-buzz`                      | `-out`                                                                                                        |  
_\*Must use variation_

### Hover Background Animations

| Background Animation  | Main Class(es)                  | Variations/Add-Ons                                                                                         |
| --------------------- | ------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| Fade                  | `hvr-fade`                      | none                                                                                                       |
| Pulse                 | `hvr-back-pulse`                | none                                                                                                       |
| Sweep\*               | `hvr-sweep-to`                  | `-top`, `-right`, `-bottom`, `-left`                                                                       |
| Bounce\*              | `hvr-bounce-to`                 | `-top`, `-right`, `-bottom`, `-left`                                                                       |
| Radial\*              | `hvr-radial`                    | `-in`, `-out`                                                                                              |
| Rectangle\*           | `hvr-rectangle`                 | `-in`, `-out`                                                                                              |
| Shutter In\*          | `hvr-shutter-in`                | `-horizontal`, `-vertical`                                                                                 |
| Shutter Out\*         | `hvr-shutter-out`               | `-horizontal`, `-vertical`                                                                                 |  
_\*Must use variation_

### Hover Border Animations

| Border Animation      | Main Class(es)                  | Variations/Add-Ons                                                                                         |
| --------------------- | ------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| Fade                  | `hvr-border-fade`               | none                                                                                                       |
| Hollow                | `hvr-hollow`                    | none                                                                                                       |
| Trim                  | `hvr-trim`                      | none                                                                                                       |
| Ripple\*              | `hvr-ripple`                    | `-in`, `-out`                                                                                              |
| Outline\*             | `hvr-outline`                   | `-in`, `-out`                                                                                              |
| Round Corners         | `hvr-round-corners`             | none                                                                                                       |
| Underline\*           | `hvr-underline-from`            | `-center`, `-left`, `-right`                                                                               |
| Overline\*            | `hvr-overline-from`             | `-center`, `-left`, `-right`                                                                               |
| Reveal                | `hvr-reveal`                    | `-underline`, `-overline`                                                                                  |  
_\*Must use variation_

### Hover Misc Animations

| Misc. Animations         | Main Class(es)                    | Variations/Add-Ons                                                                                    |
| ------------------------ | -------------------------------   | ----------------------------------------------------------------------------------------------------- |
| Curling Corner\*         | `hvr-curl-bottom`, `hvr-curl-top` | `-left`, `-right`                                                                                     |
| Glow                     | `hvr-glow`                        | none                                                                                                  |
| Shadow                   | `hvr-shadow`                      | `-grow`                                                                                               |
| Shadow Advanced\*        | `hvr-shadow`                      | `-inset`, `-outset`, `-float`, `-radial`                                                              |
| Speech Bubble\*          | `hvr-bubble`                      | `-top`, `-right`, `-bottom`, `-left`                                                                  |
| Floating Speech Bubble\* | `hvr-bubble-float`                | `-top`, `-right`, `-bottom`, `-left`                                                                  |   
_\*Must use variation_

## Thank You
Again I'd like to give a shout out to [Daniel Eden](https://daneden.github.io/animate.css "Daniel Eden") for his animations and to [Ian Lunn](https://ianlunn.github.io/Hover) for his hover animations. Like I said earlier, this project has been to learn more about the LESS language and so I'm extremely grateful I didn't have to write the animations from scratch.
