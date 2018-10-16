# Slides template

This a template for [Backslide](https://github.com/sinedied/backslide).
Basically, a bunch of modified Sass from the starter theme Backslide comes with.

![](template.png)

Check out a [demo](http://coopdevs.org/assemblea_katuma_30_05_2018/).

## Installation

First, ensure your presentation project has a `package.json`. You can create one
running `npm init`. This will walk you through the process step by step.

Then, add the `slides_template` dependency doing

```sh
$ npm install slides_template --save
```

## Usage

You need to provide the `--template` argument when initializing a new
presentation as follows:

```sh
$ node_modules/backslide/bin/bs init --template node_modules/slides_template/template/
```

This will create a `presentation.md` file where you can edit your slides.

Check out [Backslide's docs](https://github.com/sinedied/backslide#usage) for
more details.
