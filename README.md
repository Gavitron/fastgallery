# fastgallery [![Go Report Card](http://goreportcard.com/badge/tonimelisma/fastgallery)](http://goreportcard.com/report/tonimelisma/fastgallery) ![GitHub release (latest SemVer)](https://img.shields.io/github/v/release/tonimelisma/fastgallery) ![License](https://img.shields.io/badge/license-MIT-blue.svg) [![Build Status](https://github.com/tonimelisma/fastgallery/workflows/build/badge.svg)](https://github.com/tonimelisma/fastgallery/actions) [![Coverage Status](https://img.shields.io/coveralls/github/tonimelisma/fastgallery)](https://coveralls.io/github/tonimelisma/fastgallery?branch=master)

## Fast static photo and video gallery generator

- Super fast (written in Go and C, concurrent, uses fastest image/video libraries, 4-8 times faster than others)
- Both photo and video support
- Deals with any file formats (including HEIC and HEVC)
- Only updates changed files, runs incrementally
- If aborted, can continue from where it stopped and clean-up unfinished files
- Will delete removed source files from gallery
- Uses relative paths (safe for using in subdirectory or S3)
- Minimal bloat (vanilla JS frontend, minimal CSS)

## Examples

Please see [https://www.melisma.net/fastgallery-examples/](https://www.melisma.net/fastgallery-examples/)

## Dependencies

### MacOS

For dependencies, use Homebrew to install:

`brew install vips ffmpeg`

### Ubuntu Linux

For Ubuntu 18.04 bionic or 20.04 focal, first add my PPA for latest libvips with HEIF support:

`sudo add-apt-repository ppa:tonimelisma/ppa`

Then install libvips42 for images and optionally ffmpeg (if you need video support):

`apt-get install libvips42 ffmpeg`

## Install

1. Download the latest release
2. Run ```make build```
3. Copy ```bin/fastgallery``` to ```/usr/local/bin```

## Usage

`fastgallery ~/Dropbox/Pictures /var/www/html/gallery`

## Roadmap

For the prioritised roadmap, please see <https://github.com/tonimelisma/fastgallery/projects/1>

## Third party libraries

- [govips](https://github.com/davidbyttow/govips), lightning fast image processing and resizing library in Go/C
- [Feather](https://github.com/feathericons/feather) icons, simple and beautiful
- [Primer](https://github.com/primer/css) CSS, Github's in-house design system
