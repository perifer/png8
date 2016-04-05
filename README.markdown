png8 is a commandline tool for OS X that converts 24-bit PNG images to 8-bit PNG. 
Most common graphic programs can't export to 8-bit PNG with alpha transparency
even though it's by far the most useful file format for the web.

Further reading on the advantages of 8-bit PNG:

http://www.sitepoint.com/png8-the-clear-winner  
http://html5boilerplate.com/docs/Notes-on-using-png  
http://calendar.perfplanet.com/2010/png-that-works  

## Features

* Uses two different converters (pngquant and pngnq) with sane defaults and options.
* Converts several files at once and ignores files that already are 8-bit PNG.
* Preview different alternatives and choose the best one (interactive mode).
* Uses pngout if available to further reduce file size.

## Installation

    curl https://raw.githubusercontent.com/perifer/png8/master/png8 >> /usr/local/bin/png8 && chmod u+x /usr/local/bin/png8

Download and install dependencies manually:

[pngquant](http://pornel.net/pngquant)  
[pngnq](http://pornel.net/pngnq)  
[pngout](http://www.jonof.id.au/pngout)  

Or install with homebrew:

    brew install pngquant
    brew install pngnq
    brew install jonof/kenutils/pngout

## Examples

Convert file.png with pngquant and create a backup of the original file:

    png8 file.png

Skip backup (Overwrite) and convert all PNGs in a specific directory. 8-bit PNGs in the same directory are ignored:

    png8 -O images/*.png
    
Preview different alternatives (interactive) and save to directory "img":

    png8 -i file.png -d img
    
List all options:

    png8 --help
