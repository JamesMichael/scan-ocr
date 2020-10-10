# scan-ocr

Simple script to scan, ocr, and combine documents into a single PDF.

I've been using this script to digitize my important documents and clear out
my filing cabinet.

## Requirements

Software Requirements:

* [ImageMagick](https://imagemagick.org/)
* [SANE](http://www.sane-project.org/)
* [Tesseract OCR](https://tesseract-ocr.github.io/)
* [qpdf](http://qpdf.sourceforge.net/)

Hardware Requirements:

You'll need a scanner compatible with SANE, and already configured.

## Running

Designed to be run with minimal configuration and to do-the-right-thing.

You'll need to pass the scanner device name into the script, either by
modifying the `DEVICE` variable, setting the `DEVICE` environment variable,
or passing it in as a parameter to the `--device` option.

Run as `./scan --device NAME`, press Enter to start scanning (then Enter to
continue scanning additional pages) followed by Control-D to stop scanning.
A pdf will be output in the current directory.


The `--grayscale` flag can be used when scanning grayscale documents to add some
grayscale-specific optimisations.

The `--quality` flag sets the quality (between 0-100, default 80) of the output
document and applies various filters to the output depending on the level chosen.

An optional filename can be provided as the last argument to change the
destination filename (default ocr.pdf).

See the output of `./scan --help` for detailed options.
