<img src="https://raw.githubusercontent.com/ornicar/chessground/master/screenshot/3d.png" width=512 height=512 alt="Chessground in 3D mode" />

**Chessground** is the opensource chess UI developed for [lichess.org](http://lichess.org).

It targets modern browsers, as well as mobile development using Cordova.

### Demos

- [Chess TV](http://lichess.org/tv)
- [Board editor](http://lichess.org/editor)
- [Puzzle solver](http://lichess.org/training)
- [Analysis board](http://lichess.org/ofWXRFGy)
- [Game preview](http://lichess.org/games)
- [Chess Captcha](http://lichess.org/signup)

## Features

Chessground is designed to fulfill all lichess.org web and mobile apps needs, so it is pretty featureful.

- Well typed with typescript
- Fast. Uses a custom DOM diff algorithm to reduce DOM writes to the absolute minimum
- Small footprint: 10K gzipped (31K unzipped). No dependencies.
- SVG drawing of circles and arrows on the board
- Entirely configurable and reconfigurable at any time
- Styling with CSS only: board and pieces can be changed by simply switching a class
- Fluid layout: board can be resized at any time
- Support for 3D pieces and boards
- Full mobile support (touchstart, touchmove, touchend)
- Move pieces by click
- Move pieces by drag'n drop
  - minimum distance before drag
  - centralisation of the piece under the cursor
  - piece ghost element
  - square over elements
  - drop off revert or trash
- Premove by click or drag
- Animation of pieces: moving and fading away
- Display last move, check, move destinations, and premove destinations
- Import and export positions in FEN notation
- User callbacks
- No chess logic inside: can be used for chess variations

## Installation

```
npm install --save chessground
```

### Usage

```js
var Chessground = require("chessground").Chessground;

var ground = Chessground(document.body, config);
```

## Documentation

- [Config documented types](https://github.com/ornicar/chessground/tree/master/src/config.ts)
- [Config default values](https://github.com/ornicar/chessground/tree/master/src/state.ts)
- [API documented type signatures](https://github.com/ornicar/chessground/tree/master/src/api.ts)
- [Examples repo](https://github.com/ornicar/chessground-examples/tree/master/src/units)
- [Base CSS](https://github.com/ornicar/chessground-examples/blob/master/assets/chessground.css)

## Developers

First of all, of course:

```
npm i
```

To build the node module:
```
tsc -watch
```

To build the standalone:

```
gulp dev  // build once
gulp      // build and watch
gulp prod // build minified
```
