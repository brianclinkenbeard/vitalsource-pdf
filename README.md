# vitalsource-pdf
vitalsource-pdf is a simple, fully POSIX compliant shell script to create PDFs of pages from a textbook on VitalSource for printing. It uses `curl` to fetch the pages of the textbook and `img2pdf` (or, alternatively, ImageMagick's `convert`) to convert the pages to a PDF.

It is recommended to install josch's [img2pdf](https://gitlab.mister-muffin.de/josch/img2pdf) before running this script. If vitalsource-pdf does not detect the `img2pdf` executable to be installed, it will allow the user to optionally fall back on ImageMagick for lossy and possibly more resource intensive conversion. See the img2pdf README for a greater comparison between the tools.

## Usage
```
Usage: ./vitalsource-pdf [-c <cookie>] [-i <isbn>] [-s <start page>] [-n <number of pages>]
```
To find your cookie, use the developer tools on Firefox or Chrome after logging in to VitalSource. The cookie string should contain `_jigsaw_session`.
