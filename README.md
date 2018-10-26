# Slides template

This a template for [Backslide](https://github.com/sinedied/backslide).
Basically, a bunch of modified Sass from the starter theme Backslide comes with.

![](template.png)

Check out a [demo](http://coopdevs.org/assemblea_katuma_30_05_2018/).

## Requirements

* npm >= 5.2.0

Check [npm installation](https://www.npmjs.com/get-npm) instructions if you don't have it yet.

## Installation

First, ensure your presentation project has a `package.json`. You can create one
running `npm init`. This will walk you through the process step by step.

Then, add the `backslide` and `slides_template` dependencies doing

```sh
$ npm install backslide slides_template --save
```

## Usage

You need to provide the `--template` argument when initializing a new
presentation as follows:

```sh
$ npx bs init --template node_modules/slides_template/template/
```

This will create a `presentation.md` file where you can edit your slides.

Then, watch the resulting presentation live-reload while you work on it by running:

```sh
$ npx bs serve
```

Once finished, you can export them to PDF with the following command:

```sh
$ npx bs pdf
```

Check out [Backslide's docs](https://github.com/sinedied/backslide#usage) for more details.
