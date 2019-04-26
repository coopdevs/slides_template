# Slides template

This a template for [Backslide](https://github.com/sinedied/backslide).
Basically, a bunch of modified Sass from the starter theme Backslide comes with.

![](template.png)

Check out a [demo](http://coopdevs.org/assemblea_katuma_30_05_2018/).

## Requirements

* npm >= 8.11

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

## Themes

To choose a different theme, fetch all branches and switch to a theme branch. So far, there is only `green-theme` and `master`, which implements the blue theme shown at the top of this file.

While we don't find a better mechanism to handle themes, theme branches need to be kept up to date with changes in `master`, which means that they'll need to be rebased onto `master` as soon as changes happen.

## Troubleshooting

Sometimes you might get the following error when running `npx bs init` as described above.

```
ENOENT: no such file or directory, scandir '/home/pau/dev/OFN_sobtec_2019/node_modules/node-sass/vendor'
```

Running `npm rebuild node-sass` fixes it.

### Failure installing puppeteer

If you see the following failure when installing dependencies

```
npm WARN optional Skipping failed optional dependency /chokidar/fsevents:
npm WARN notsup Not compatible with your operating system or architecture: fsevents@1.2.8
npm WARN katuma_ofn_information_systems_talk@1.0.0 No repository field.
npm ERR! Linux 4.15.0-47-generic
npm ERR! argv "/home/pau/.nodenv/versions/5.12.0/bin/node" "/home/pau/.nodenv/versions/5.12.0/bin/npm" "install" "backslide" "slides_template" "--save"
npm ERR! node v5.12.0
npm ERR! npm  v3.8.6
npm ERR! code ELIFECYCLE

npm ERR! puppeteer@1.12.2 install: `node install.js`
npm ERR! Exit status 1
npm ERR!
npm ERR! Failed at the puppeteer@1.12.2 install script 'node install.js'.
npm ERR! Make sure you have the latest version of node.js and npm installed.
```

it is because you are using and old version of node. Install at least node 8.11 and try again.
